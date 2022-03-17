# IOTools

## Table of contents

* [General info](#general-info)
* [Example](#example)
* [Dependencies](#dependencies)

## General info

Simple reader/writer and converters for NIfTI images and vtkPolydata

| Features                               | Status              |
|----------------------------------------|---------------------|
| NIfTI reader                           | :white_check_mark:  |
| NIfTI writer                           | :white_check_mark:  |
| vtkPolydata reader                     | :white_check_mark:  |
| vtkPolydata writer                     | :white_check_mark:  |
| binary mask to polydata                | :white_check_mark:  |
| polydata to binary mask | :white_check_mark:  |

Bastien Rigaud, PhD Laboratoire Traitement du Signal et de l'Image (LTSI), INSERM U1099 Campus de Beaulieu, Université
de Rennes 1 35042 Rennes, FRANCE bastien.rigaud@univ-rennes1.fr

## Example

```python
# mask to polydata
converter = DataConverter(image=image, inval=1, outval=0, cast_float32=True)
input_features[output_key] = converter.mask_to_polydata()

# polydata to mask
input_converter = DataConverter(polydata=input_polydata, cast_float32=False)
input_mask = input_converter.polydata_to_mask()
```

## Dependencies

```
pip install -r requirements.txt
```