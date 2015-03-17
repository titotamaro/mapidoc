# Introduction

This is the public repo for the documentation of the Materials API. The 
Materials API is a simple, flexible and efficient interface to programmatically
query and interact with the Materials Project database based on the
REpresentational State Transfer (REST) pattern for the web. Since its creation
in Aug 2012, the Materials API has been the Materials Project’s de facto
platform for data access, supporting not only the Materials Project’s many
collaborative efforts but also enabling new applications and analyses.

# Using this repo

The usage of this repo is very simple and in fact, follows as REST format. The
primary use of this repo is to explore the Materials Project's document format
and use that info for much more powerful queries with the pymatgen (Python
Materials Genomics) MPRester.query method. For more standard queries, the
Materials API already has a wiki and pymatgen already provides useful high-level
functions for them.

1. Start from the docs directory. The nested directory structure follows the
   json document schema for the Materials Project's materials collection.
2. In each folder, there is a README.md that describes what that key is. For
   example, in docs/final_energy, the README.md informs you that this key refers
   final calculated energy of the material.
3. To use this in MPRester, one may use the following code::

```python
from pymatgen import MPRester
m = MPRester()
m.query(criteria={"task_id": "mp-1234"}, properties=["final_energy"])
```

# Citing

If you use the Materials API extensively, you may wish to cite the following 
publication::

	(1) Ong, S. P.; Cholia, S.; Jain, A.; Brafman, M.; Gunter, D.; Ceder, G.; 
	Persson, K. a. The Materials Application Programming Interface (API): A 
	simple, flexible and efficient API for materials data based on
	REpresentational State Transfer (REST) principles, Comput. Mater. Sci.,
	2015, 97, 209–215, doi:10.1016/j.commatsci.2014.10.037.
