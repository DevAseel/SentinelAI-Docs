---
sidebar_position: 2
---

# convert_pdf_to_images()

`convert_pdf_to_images()` method is the starting step for tabular data ingestion and it works as the following:

<img src="https://sentinel-ai-docs.vercel.app/img/pdf_to_images.png" />

## Usage

- Place the pdf file you would like to process in `./pdfs` directory.
- Find the execution file at `./convert_pdf_to_images.py` and run the following command:

```bash
    python pdf_to_images_converter.py --log-level debug --pdf-name <your-pdf-name>
```

## Parameters

| Parameter          | Description                                                                     | Type   | Required | Default            | Options                                         |
|--------------------|---------------------------------------------------------------------------------|--------|----------|--------------------|-------------------------------------------------|
| --pdf-name         | the name of the pdf file inside `./pdfs` directory wihout the `.pdf` extension  | string | &check;  | _                  | _                                               |
| --output-directory | the relative path to the output directory where the images will be stored       | string | &cross;  | `./outputs/images` | _                                               |
| --log-level        | the level of the log messages you would like to display when executing the file | string | &cross;  | `info`             | `debug`, `info`, `warning`, `error`, `critical` |
