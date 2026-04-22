{{- /* Static header */ -}}
# {{ .Site.Title }}: replicated key-value database backed by object storage.

> Netsy is an Open Source, replicated key-value database which stores data in object storage. It implements a subset of the etcd API (Range, Txn, Watch) and can be used as a drop-in etcd replacement for Kubernetes or as a general-purpose KV store for applications that need durable, low-latency persistence without the operational complexity of running a traditional database.

- Website: {{ .Site.BaseURL }}
- GitHub: https://github.com/netsy-dev/netsy
- LLMs.txt: {{ .Site.BaseURL }}llms.txt

## Documentation
{{ with .Site.GetPage "/docs" }}
{{- range .RegularPages }}
- [{{ .Title }}]({{ .Permalink | strings.TrimRight "/" }}.md){{ with .Description }}: {{ . }}{{ end }}
{{- end }}
{{ range .Sections }}
### {{ .Title }}
{{ with .Description }}
> {{ . }}
{{ end }}
{{- range .Pages }}
- [{{ .Title }}]({{ .Permalink | strings.TrimRight "/" }}.md){{ with .Description }}: {{ . }}{{ end }}
{{- end }}
{{ end }}
{{- end }}
---

Tip: Append `.md` to any page URL to get the markdown version.