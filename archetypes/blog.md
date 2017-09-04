+++
title = "{{ replace .TranslationBaseName "-" " " | title }}"
date = {{ .Date }}
description = ""
draft = true
hidden = true
slug = "{{ dateFormat "2006-01-02" .Date }}/{{ replace .TranslationBaseName "-" " " | title | urlize }}"
+++
