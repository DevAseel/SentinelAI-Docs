---
sidebar_position: 6
---

# table_constructor()

`table_constructor()` class is used after `tables_scanner()` to construct tables by defining rows for detected tables. The method loads the OCR model for table structure recognition and returns a json object containing the bounding boxes of the detected cells in the table.

<img src="https://sentinel-ai-docs.vercel.app/img/table_constructor.png" />

## Usage

- Find the execution file at `./table_constructor.py` and run the following command:

```bash
    python table_constructor.py --img-path <path-to-cropped-table-image> --log-level debug
```
- To output the results as a `json` file, you can use the following command:

```bash
    python table_constructor.py --img-path <path-to-cropped-table-image> --json true
```
- To specify an output path for the json file, you can use the following command:

```bash
    python table_constructor.py --img-path <path-to-cropped-table-image> --json true --json-path <path-to-json-file>
```

- You can also customize the OCR model and the device type to load the model by providing the model repository and device type as arguments:

```bash
        python table_constructor.py --img-path <path-to-your-image> --model-name <model-repository> --device <device-type>
```


## Parameters

| Parameter           | Description                                                                              | Type    | Required | Default                                          | Options                                                              |
|---------------------|------------------------------------------------------------------------------------------|---------|----------|--------------------------------------------------|----------------------------------------------------------------------|
| \--img-path         | the relative path of the image                                                           | string  | ✓        | \_                                               | \_                                                                   |
| \--model-name       | the name of the OCR model to be used for table structure recognition                     | string  | ✗        | `microsoft/table-structure-recognition-v1.1-all` | \_                                                                   |
| \--device           | the device type to load the model (cpu, cuda, mkldnn, opengl, opencl, ideep, hip, msnpu) | string  | ✗        | `cpu`                                            | `cpu`, `cuda`, `mkldnn`, `opengl`, `opencl`, `ideep`, `hip`, `msnpu` |
| \--output-directory | the directory to save the output image with detected cell bounding boxes                 | string  | ✗        | `./outputs/constructed_tables`                   | \_                                                                   |
| \--json             | set true to save output as a json file                                                   | boolean | ✗        | `false`                                          | `true`, `false`                                                      |
| \--json-path        | add to set a custom path for the saved json file                                         | string  | ✗        | `./outputs/constructed_tables_json`              | \_                                                                   |
| \--log-level        | the level of the log messages you would like to display when executing the file          | string  | ✗        | `info`                                           | `debug`, `info`, `warning`, `error`, `critical`                      |
