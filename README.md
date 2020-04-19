
## Installation

Linux:
```sh
git clone https://github.com/ostis-apps/ostis-prosem.git
cd ostis-prosem/scripts
./install_ostis.sh
```

## Build knowledge base
Linux:
```sh
cd ostis-prosem/ostis/scripts
./build_kb.sh
```

## Run
Run on Linux:
```sh
#Terminal 1
cd ostis-prosem/ostis/scripts
./run_sctp.sh

#Terminal 2
cd ostis-prosem/ostis/scripts
./run_scweb.sh
```

Then open localhost:8000 in your browser

## Project Structure

### kb
Place for knowledge base of your app. Put your **.scs** and **.gwf** files here.

### problem-solver
Place for problem solver of your app. Put your agents here.

#### Agents on C++
Some tips:
- Store your modules with c++ agents in *problem-solver/cxx*;
- After update c++ code you need to rebuild sc-machine. Just run:  
```
cd {project-name}/ostis/sc-machine/scripts
./make_all.sh
```
- For enable debug:
    * add *SET(CMAKE_BUILD_TYPE Debug)* line 
    to *ostis-prosem/ostis/sc-machine/CMakeLists.txt* file;
    * rebuild sc-machine.
- Look example module with C++ agent [here](problem-solver/cxx/exampleModule/README.md).

### interface

Place for your interface modules.

#### sc-web-extensions
Place for your extensions of standard **IMS interface(sc-web)**. 

*We don't have automatically applying of your extensions to sc-web now. Do it by hand.*
