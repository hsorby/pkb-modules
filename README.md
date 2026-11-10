# pkb modules

The enterocyte model (enterocyte-modules) extended with a hepatocyte and a body loop. Same layout and format as enterocyte-modules. Generated from `pkb-model.json`.

| Module type | Instances |
|---|---|
| `compartment` | `lumen`, `enterocyte`, `capillary_gut`, `capillary_liver`, `hepatocyte`, `body` |
| `GLUT2` | `GLUT2_api`, `GLUT2_bas`, `GLUT2_bas_liver` |
| `SGLT1`, `NKA`, `Kir`, `membrane` | `SGLT1`, `NKA`, `Kir`, `Membrane` |
| `advection` | `portal_vein`, `hepatic_vein`, `systemic_circ` |
| `metabolism` | `metabolism` |

- `math/<module_type>.cellml`: one CellML 2.0 model per type. Each holds the units it uses, then its one component. Models import components from these files.
- Every variable and component has an id. The ids the annotations already used are kept. The rest come from libcellml's Annotator, which numbers them per file.
- `math/<module_type>.ttl`: annotations keyed by those ids. advection and metabolism are not annotated yet.
- `configurations/<module_type>_<instance>_modules_config.json` and `parameters/<instance>_parameters.json`: one of each per instance.
