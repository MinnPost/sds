# SDS (Simple Dataset Syndication)

SDS is a simple protocol/standard/specification for describing datasets.  It 
should be pubished alongside datasets so taht consumers of the datasets 
(both human and machines) can understand the metadata of the dataset in a
standard way.

## NOT EVEN A DRAFT

This is just an idea at the moment.  We want to create a community
around this idea and help make it a real standard.

## Get Involved

Email: ??

## What are Datasets?

Datasets are any structured, non-API sources of data.  For example:

* CSV file
* JSON feed
* RSS feed
* XML document
* Shapefile
* ??

This needs more definition.  It is difficult to determine where
an API begins and a data feed ends.  This could be helpful:
http://en.wikipedia.org/wiki/Data_set

## Example

The following is an (brainstorming) example of an SDS feed in JSON
for a CSV file.

```
  {
    "sds_version": "0.1",
    "set_name": "Our Example Set",
    "set_description": "Our Example Set is pretty great.",
    "datasets": [
      {
        "type": "csv",
        "url": "http://example.com/datasets/data.csv",
        "name": "CSV File",
        "description": "CSV is still useful and simple.",
        "author": "Author"
        "origin": {
          "author": "Example Original Author",
          "organization": "Example Org",
          "url": "http://example.gov/dept/data-service/"
        },
        "fields": {
          "field_1": "Description of field 1",
          "field_2": "Description of field 2",
          "field_3": "Description of field 3",
          "field_4": "Description of field 4"
        },
        "type_info": {
          "version": "CVS version X",
          "delimiter": ",",
          "line_separator": "\r\n"
        }
      }
    ]
  }
```