## Support
- [x] coco2xml_convert
- [x] xml2coco_convert

## Usages

### Convert coco format to voc xml format
```python
from volkscv.utils.converter import coco2xml_convert

def test_coco2xml():
    """ 
    Args:
        anno_file (str): Path to annotations of data.
        output_dir (str): Path to save folder.
        folder_split (bool): If true, it will store file into different directories 
                            under output dir based on their categories. 
    Format:
        anno_file:
        
    """
    coco2xml_convert(anno_file='instances_val2014_.json',
                     output_dir='./result')

```
### Convert voc xml format to coco format

```python
from volkscv.utils.converter import xml2coco_convert


def test_xml2coco():
    """ 
    Args:
        xml_list (str): Path to annotation files ids list.
        xml_dir (str): Path to annotation files directory.
        categories (list or tuple): Categories.
        json_file (str): Path to output json file.
        start_cate_id (int): Start id of categories. Default: 1.
 
    Format:
        xml_list:
        
        
    """
    xml2coco_convert(xml_list='data/overfit.txt',
                     xml_dir='data/Annotations',
                     json_file='./output.json')

```
