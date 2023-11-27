# Introduction

**FIREBALL** was originally developed in 1989 by renowned physicist Otto F. Sankey, and has since continued to evolve its functionality. FIREBALL focuses on quantum mechanics-based molecular dynamics simulations, studying the dynamic evolution and excitation processes in energy conversion processes, understanding and controlling mass and energy transfer in materials during chemical reactions from a quantum perspective. The software SIESTA was also originally based on FIREBALL. The review article by Professor Lewis about FIREBALL was selected by Physica Status Solidi as the issue Highlight. Additionally, this paper was discussed by McNellis in Materials Views online who stated that “The numerical technology at the heart of FIREBALL offers chemically relevant predictions in exceptionally large models…. This guarantees that FIREBALL will remain relevant in the future….”. More than 1,000 scientific research articles have been published in international journals based on FIREBALL software. The code is currently maintained by Professor James P. Lewis. The latest version of FIREBALL is open source, including 100,000+ lines of Fortran (Fortran version 2003 and above)

[ASE](https://wiki.fysik.dtu.dk/ase/index.html) is a popular python package for atomic structure modeling. ASE provide interfaces with many QM and MM software. The [Thunder-ASE](https://github.com/thunder-dft/thunder-ase) package is not only the ASE interface for FIREBALL, but also provides many other useful functions. It is recommended that use [thunder-ASE](https://github.com/thunder-dft/thunder-ase) to run FIREBALL instead of run it directly. The following [tutorials]() are all using [thunder-ASE](https://github.com/thunder-dft/thunder-ase).

**Simple example**

```Python
from thunder_ase.fireball import Fireball
from ase.build import molecule

atoms = molecule('C6H6')
Fdata_path = 'YOUR_FDATA_PATH'

kwargs = {'iwriteout_charges': 1,  # Writing out the charges.
          'efermi_T': 200.0,
          }

calc = Fireball(command='YOUR_PATH for fireball.x', 
                Fdata_path=Fdata_path,
                **kwargs)
atoms.calc = calc

e0 = atoms.get_potential_energy()
efermi = atoms.calc.get_fermi_level()

print("The energy is {:.3f} eV.".format(e0))
print("The Fermi Level is {:.3f} eV.".format(efermi))
```
