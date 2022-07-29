# diamond_structure_vasp

vasper_final_0_jun20

The script 'vasper_final_0_jun20' is made in BASH.

It is the general code that helped me to get my bachelor's degree in Physics. https://riull.ull.es/xmlui/handle/915/29103

I connected via ssh protocol to a server at my university and did the calculations remotely.

I used the program VASP (Vienna Ab Initio Package) with version vasp.5.3.5o2.

It runs from a directory 'main' and you need to create a directory within main that contains a directory for each material to be studied. 
This script does it for materials with only one POTCAR file for each material, so they must be of one atom type. 
In my case it was the structure of diamond in both hexagonal and cubic form for carbon, silicon, germanium and tin. 

Once created a lowercase directory for each material such as " 'c', 'si', 'ge', 'sn' , 'lonsdaleiteC', 'lonsdaleiteSi', 'lonsdaleiteGe', 'lonsdaleiteSn' ". 
Once these directories have been created, they must each contain three directories 'mcases', 'summary', 'temporary' and a POTCAR file (the one for the corresponding material). 
Inside the 'mcases' directory we will create 2 more called 'case1', 'case2'. In each of them we will study different properties. 
Each of them will be linked to their respective INCAR, POSCAR and KPOINTS files belonging to the Inputs of the VASP program.

When it is executed, after the calculation in the summary directory of each material you will find the outputs in flat data files and placed in two columns with header.

The directory path:

main
  material
    c
      mcases 
        case1
          POSCAR
          KPOINTS
          INCAR
        case2
      POTCAR
      temporal
      summary
      
    si
    ge
    sn
    lonsdaleiteC
    lonsdaleiteSi
    lonsdaleiteGe
    lonsdaleiteSn
    
