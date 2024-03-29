# OPF - the open pecha format

OPF is an open-directory file format containing a text and its annotations in an easy to parse, metadata and optionally the source of the text. 

Metadata structure in OpenPecha is based on the [BibFrame2](https://www.loc.gov/bibframe/docs/bibframe2-model.html) model, while annotations follow the TEI standard as much as possible.

There are two types of .opf documents, the Work files and the Pecha files. Works are BibFrame2 works and Pechas correspond to BibFrame2 Instances. Thus a Work can have multiple Pechas. Exact digital duplicates are recorded as Items in the Work metadata.

As a policy, we don't try to avoid duplication but try to record all instances (Pechas) of a given text in the corresponding work.


## W######.opf

## /meta.yaml


## P######.opf

## /meta.yaml
- scr : # link to source documents
    - images IIIF work
    - ocr output like Google's jsons
    - manual input in epub, pdf, docx, txt
- layers: # description of layers
    - pagination # page information from the image source, doesn't include line information, includes blank pages
    ![image](https://user-images.githubusercontent.com/17675331/69866208-70a32080-12de-11ea-817d-79a4a57e94fc.png)
        - 1 arabic number
        - 2 vol name
        - 3 vol tag
        - 4 bo number

## /index.yaml
- the base directory contains raw text, 1 file per volume

## /base/
- the base directory contains raw text, 1 file per volume
- UTF-8
- base contains line returns matchinng lines from source images, or random segmentation for other formats
- base layer doesn't contain metadata like page numbers, page titles, footnotes and the like. These are encoded in layers

## /layers/
- layers 
- UTF-8
- 

