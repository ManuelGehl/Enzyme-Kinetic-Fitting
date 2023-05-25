# Enzyme-kinetic-fitting
Takes Excel files with specific activity measurements for enzymes (and corresponding mutants) and does a curve fitting to the Michaelis-Menten equation. I used this code for determining the kinetic constants of wild type and mutated enzymes, e.g. in  Gehl, M, Demmer, U, Ermler, U, Shima, S. Crystal structure of FAD-independent methylene-tetrahydrofolate reductase from Mycobacterium hassiacum. Proteins. 2023; 1- 12. doi:10.1002/prot.26504
It works best with an Excel file that has the name of the corresponding mutant as tab name (e.g. "WT" or "E9Q"). For my case I had the columns "nadh", "h4f","specific activity 1","specific activity 2","specific activity 3","mean","stdev" and as rows the corresponding substrate concentrations.

