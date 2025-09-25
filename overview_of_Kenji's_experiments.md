

# From PI to LGM
| suite-id | years     | comment                                   | site |
| -------- | --------- | ----------------------------------------- |------|
| bm847  | - | HadGEM3-GC3.1 N96ORCA1 PI Control for CMIP6 |MetO-Cray|
| by975  | - | PI Control for CMIP6 WITH LGM orbits and CO2 |MetO-Cray|
| bz669  | - | PI LSM, LGM GHGs, orbit & icesheets |MetO-Cray|
| bz669  | - | PI LSM, LGM GHGs, orbit & icesheets |MetO-Cray|
| cj345  | - | HadGEM3-GC3.1 N96ORCA1 - PI Control std Suite for CMIP6 - 1 year test |archer2|
| cj788  | - | HadGEM3-GC3.1 N96ORCA1 - PI Control with the LGM CO2 and orbital parameters (1 year test) from cj345 |archer2|
| cj841  | - | HadGEM3-GC3.1 N96ORCA1 - PI Control with the LGM CO2 and orbital parameters, and ice-sheets on the PI LSM (1 year test) from cj788 |archer2|
| cq703  | - | the most stable simulation for the LGM,This suite is based on nearly the LGM boundary condition, but the Southern Hemisphere (S60-S90) uses a modern land-sea mask with LGM topography because the LGM model errors originated from the Southern Ocean (very close to Antarctica). from cj841|archer2|
| cj986  | - | full LGM simulation for CMIP6-PMIP4. v1 from cj841 |archer2|
| co328  | - | full LGM simulation, crashed every 2-5 years from cj986|archer2|
| cv921  | - | HadGEM3-GC3.1 N96ORCA1 - the LGM full simulation for CMIP6-PMIP4. v7，modified based on cq703 | archer2 |
| db646  | - | HadGEM3-GC3.1 - the LGM simulation with the ozone remapping scheme after ARCHER2 OS upgrade |archer2|


diff -ur cj788 cj345
find that
```
  -um_sources=branches/pkg/Share/vn10.7_CMIP6_production_mods@43043 branches/dev/kenjiizumi/vn10.7_orbital_21k
  +um_sources=branches/pkg/Share/vn10.7_CMIP6_production_mods@43043
```
the pathes in fact means the codes stored in the repository: **fcm:um.xm**
```
fcm ls fcm:um.xm/branches/dev/kenjiizumi/vn10.7_orbital_21k
```
checkout it by fcm co fcm:um.xm/branches/dev/kenjiizumi/vn10.7_orbital_21k
the next step is to compare these two resource directory.

## My test ##
u-ds929: copy of u-cv921

