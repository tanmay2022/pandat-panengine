I am creating this repository for refering to pandat/panengine workflow.

## Getting composition from panengine source:

* Declare temperature range and alloy components in composition.cpp

* To create object file:

> g++-4.8 -c composition.cpp -Wall -fexceptions -std=c++0x -DPANENGINE -DPANPRECIPITATION -O3 -c

* To create executable:

> g++-4.8 -o main2 PanEngineTest_1.o PanEngineTest_2.o PanEngineTest_3.o PanEngineTest_4.o PanEngineTest_5.o dendritetip.o PanEngineTest_7.o composition.o PanEngineTest_9.o main2.o -L /home/abhik/lib/linux -lPanEngineX -lboost_regex -lhasp_linux_x86_64_57714 -lPanHasp -lPanSolverX

* Execute and then choose 8:

> ./main2

* Convert test_8.dat to csv using composition_ternary.ipynb

## Getting hessian from panengine source:

* Declare temperature range and alloy components in hessian.cpp

* To create object file:

> g++-4.8 -c hessian.cpp -Wall -fexceptions -std=c++0x -DPANENGINE -DPANPRECIPITATION -O3 -c

* To create executable:

> g++-4.8 -o main2 PanEngineTest_1.o PanEngineTest_2.o PanEngineTest_3.o PanEngineTest_4.o PanEngineTest_5.o dendritetip.o PanEngineTest_7.o hessian.o PanEngineTest_9.o main2.o -L /home/abhik/lib/linux -lPanEngineX -lboost_regex -lhasp_linux_x86_64_57714 -lPanHasp -lPanSolverX

* Execute and then choose 8:

> ./main2

* Convert test_8.dat to csv using hessian_ternary.ipynb

## Getting temperature range of phases and thermal data from pandat:

* Create a new workspace -> Pan Phase Diagram

* Databases -> Load TDB of PDB -> Select components (use >).

* PanPhaseDiagram -> Line calculation -> select options -> choose units, default table (tick what you want to generate) -> ok -> enter alloy composition and temperature range -> number of steps in temperature -> ok

* Open generated table from worspace.

## Getting precipitation plots from pandat:

* Create a new workspace -> Pan Phase Diagram

* Databases -> Load TDB of PDB -> Select components (use >).

* PanPrecipitation -> Load KDB or EKDB -> Precipitation Simulation -> select options -> choose units, default table (tick what you want to generate) -> ok -> enter alloy composition and temperature range -> ok

* Open generated table from worspace.

