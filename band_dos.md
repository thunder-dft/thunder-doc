---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---


# Band and DOS calculations

In this tutorial, we perform Band and DOS calculations with a lightweight
version of FIREBALL which is called thunder-lightning.

Using the python interface [thunder-ase](https://github.com/thunder-dft/thunder-ase), 

```
    calc = Fireball(command='/path_to_lightning.x', 
                    Fdata_path=Fdata_path,
                    **kwargs)
    atoms.set_calculator(calc)
```
