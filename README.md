I am creating this repository for refering to pandat/panengine workflow.

## Getting composition from panengine source:

* To create object file:

> g++-4.8 -c in_718_comp.cpp -Wall -fexceptions -std=c++0x -DPANENGINE -DPANPRECIPITATION -O3 -c

* To create executable:

> g++-4.8 -o main2 PanEngineTest_1.o PanEngineTest_2.o PanEngineTest_3.o PanEngineTest_4.o PanEngineTest_5.o in_718_comp.o PanEngineTest_7.o hessain.o PanEngineTest_9.o main2.o -L /home/abhik/lib/linux -lPanEngineX -lboost_regex -lhasp_linux_x86_64_57714 -lPanHasp -lPanSolverX

* Execute and then choose 8:

> ./main2

* Convert test_8.dat to csv using composition_ternary.ipynb.

## Getting hessian from panengine source:

* To create object file:

> g++-4.8 -c hessain.cpp -Wall -fexceptions -std=c++0x -DPANENGINE -DPANPRECIPITATION -O3 -c

* To create executable:

> g++-4.8 -o main2 PanEngineTest_1.o PanEngineTest_2.o PanEngineTest_3.o PanEngineTest_4.o PanEngineTest_5.o hessain.o PanEngineTest_7.o hessain.o PanEngineTest_9.o main2.o -L /home/abhik/lib/linux -lPanEngineX -lboost_regex -lhasp_linux_x86_64_57714 -lPanHasp -lPanSolverX

* Execute and then choose 8:

> ./main2

* Convert test_8.dat to csv using hessian_ternary.ipynb.
