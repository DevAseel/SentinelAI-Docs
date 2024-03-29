---
sidebar_position: 8
---

# json_to_markdown_convertor()

`json_to_markdown_convertor()` method is used to convert a parsed table in JSON format to Markdown format. The resulting Markdown table can be used for easy integration into Markdown documents.


<img src="https://sentinel-ai-docs.vercel.app/img/json_to_markdown.png" />

## Usage

- Find the execution file at `./json_to_markdown_convertor.py` and run the following command:

```bash
    python json_to_markdown_convertor.py --json-path <path-to-parsed-json-table>
```


| Parameter    | Description                                                                     | Type   | Required | Default | Options                                         |
|--------------|---------------------------------------------------------------------------------|--------|----------|---------|-------------------------------------------------|
| \--json-path | the relative path of the parsed JSON table                                      | string | ✓        | \_      | \_                                              |
| \--log-level | the level of the log messages you would like to display when executing the file | string | ✗        | `info`  | `debug`, `info`, `warning`, `error`, `critical` |
