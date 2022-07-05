# mAP for the 2nd SK AI Competition

ref: https://github.com/Cartucho/map

## Modifications

* Changed IoU from 0.5 to **0.6**
* Use specified class weights to calculate mAP:
    ```python
        SK_AI_class_weights = {
            "normal": 0.17,
            "unscrewed_red": 0.23,
            "rusty_yellow": 0.17,
            "rusty_red": 0.19,
            "unscrewed_yellow": 0.19,
            "none": 0.05
        }
        sum_AP += ap * SK_AI_class_weights[class_name]
    ```

## Usage

```
python3 main.py
```

## Notes

Make sure the *input directory hierarchy* and *input file format* match that of the original source.

## TODO

Create a script to automatically create input directory structure with correct file formats from model output files