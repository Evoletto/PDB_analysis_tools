# Project Title

Proximity of lysine to light chain terminal of the disulfide bridge in Fab region of antibody

## Flow of the project:

Initial antibody .pdb files were first downloaded from the AbDB: Antibody Structure Database (http://www.bioinf.org.uk/abs/abdb/ downloaded on 13 May 2019). Downloaded dataset included Non-Redundant (NR) Kabat Antibody (Light + Heavy Fragment variable (Fv)) Datasets included total of 1483 files.

Files were first screened based on the cysteine residue being found on the C-terminus of the light chain (LC):
```
  1. FAB_Two_filters_final_whole_folder_automated.py
```
This information was extracted from the SEQRES region of the LC, once the condition was met the chain labels and the file name were identified followed by download of the full FAB antibody file from the https://www.rcsb.org.


```
  2. FAB_second_screen.py
```

```
  3. Step_through_pdb_automated.py
```

```
  3.1 run_script 
```
              -> .fit files
              -> RMSDs.txt
  4. Matrix.py
            -> matrix.txt
  5. call_out_new_zones.sh
  5.1 get_new_zones.py
  5.2 get_min_max_from_zones.py
  5.3 cut_zones_from_fit_file.py
            -> results_for_VMD.pdb
  6. Mutation
  6.1 res_mutation.py
            -> results_for_VMD_replaced.pdb
  6.2 new_chain_mutation.py
            -> results_for_VMD_replaced_vX.pdb
  6.3 chain_format.py
  7. val_distance_automatic.py
  8. histogram_final.py
  9 new_matrix_dendrogram.py