---
sidebar_position: 2
---

# tables_scanner()

`tables_scanner()` class is used after `pdf_to_images_converter()`, the method loads the OCR model for table detection and returns a json object containing the number of tables scanned and its boundry box:

<img src="https://sentinel-ai-docs.vercel.app/img/tables_scanner.png" />

## Usage

- Find the execution file at `./tables_scanner.py` and run the following command:

```bash
    python tables_scanner.py --img-path <path-to-your-image>
```
- To output the results as a `json` file, you can use the following command:

```bash
    python tables_scanner.py --img-path <path-to-your-image> --json true
```
- To specify an output path for the json file, you can use the following command:

```bash
    python tables_scanner.py --img-path <path-to-your-image> --json true --json-path <path-to-json-file>
```

- The class is utlizing `microsoft/table-transformer-detection` model as the default model, if you would like to change the model, you can pass the huggingface repository as an argument:

```bash
    python tables_scanner.py --img-path <path-to-your-image> --model <model-repository>
```


## Parameters

| Parameter          | Description                                                                     | Type   | Required | Default                                | Options                                         |
|--------------------|---------------------------------------------------------------------------------|--------|----------|----------------------------------------|-------------------------------------------------|
| --img-path         | the relative path of the image                                                  | string | &check;  | _                                      | _                                               |
| --json             | set true to save output as a json file                                          | boolean| &cross;  | `false`                                | `true`, `false`                                               |
| --json-path        | add to set a custom path for the saved json file                                | string | &cross;  | `./scanned_tables_json`                | _                                               |
| --model-name       | set to customize the OCR model                                                  | string | &cross;  | `microsoft/table-transformer-detection`| _                                               |
| --log-level        | the level of the log messages you would like to display when executing the file | string | &cross;  | `info`                                 | `debug`, `info`, `warning`, `error`, `critical` |
