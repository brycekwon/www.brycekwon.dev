+++
title = "{{ replace .Name "-" " " | title }}"
author = "{{ .Site.Params.author.name }}"
email = "{{ .Site.Params.author.email }}"
date = "{{ .Date }}"
tags = [{{ range $plural, $terms := .Site.Taxonomies }}{{ range $term, $val := $terms }}"{{ printf "%s" $term }}",{{ end }}{{ end }}]
draft = true
+++

This is a page about {{ replace .Name "-" " " | title }}.
