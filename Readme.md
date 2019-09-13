# Boolean network definition

The Boolean networks are defined in a modified `.pla` format. Each file has a
global header: 

```
pi: number of primary inputs,
po: number of primary outputs (always one in our case)
pilb: list of primary inputs,
pob: list of primary outputs (always one in our case)
f: number of nodes in the Boolean network (i.e. number of sub-functions)
```

Each sub-function starts with a header on its own:
```
i: number of inputs driving the current sub-function,
o: number of outputs of the current sub-function (always one in our case),
ilb: list of inputs driving the current sub-function,
ob: name of the sub-function,
p: number of cubes covering cR, cF, eR, and eF
```

This header is followed by cubes in the `.pla` format with the extension that in
the output part, the values `2` for "belongs to the falsified ON-set " and `3`
for "belongs to the falsified OFF-set".

Each sub-function is termined by a line containing `.e`.

# Visualizations  for the Boolean networks

The files `test4.pdf` through `test9.pdf` contain visualizations of the Boolean
networks defined in the corresponding `.pla` files.  Nodes labeled `xNN`
represent the primary inputs of the network. The other nodes represent circuits
taken from 

* S. Yang, “Logic synthesis and optimization benchmarks,” in 1989 MCNC
  International Workshop on Logic Synthesis, Dec 1988.
