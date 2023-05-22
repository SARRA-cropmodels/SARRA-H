# SARRA-H v42

This is the README file for SARRA-H version 42.

## Description

SARRA-H is both a simulation model designed for studying agricultural systems, and the Windows software that embeds it. It is a are more detailed version of the SARRA model, which is a simple dynamic water balance model used to estimate the impact of climate scenarios on annual crops. In SARRA-H, the plant is considered as a conduit that couples atmospheric demand (sink) with a "useful" water reserve in the soil (source) - a conduit with variable resistance depending on the physical constraint (stress). The SARRA-H model assume that crop performance is a simple function of accumulated water stress over a growing cycle.

SARRA-H has demonstrated good robustness across spatial scales (from plot to region) and for multiple applications, such as at the AGRHYMET early warning system for food security in the CILSS countries, local climate risk analysis, and water requirement estimation. However, its validity relies on the presence of strong water limitation and/or significant spatial or temporal variability of this limitation. In other words, this model is based entirely on growth reduction rather than simulating potential yield.

Compared to other models such as CERES, APSIM, and STICS, the SARRA-H model is deterministic and relatively simple, but simulates more processes than AQUACROP, which is a reference model proposed by FAO. SARRA-H is integrated into a flexible environment that manages a library of formalisms and a database. This model replicates plot-scale processes, enabling regional-scale analysis. Moreover, it can serve as a basic support for other scientific themes through complementary modules or interfaces with other models (meteorological, socio-economic, etc.).

Finally, the modular structure of this environment allows external management of the calculation engine (simulator) independently of the environment. All these features are described in a user manual, and the environment provides numerous tools and interfaces such as data import/export, graphical representations, sensitivity analysis, and a database to optimize data and result management.

Please refer to the documentation below for further details.

**Because of the end of life of its development platform (Borland Delphi), SARRA-H will not be maintained anymore**. We invite users to refer to our [SARRA-O](https://github.com/SARRA-cropmodels/SARRA-O-Java) and [SARRA-Py](https://github.com/SARRA-cropmodels/SARRA-Py) repositories for updates of the model and simulation platform.

## Installation

To install SARRA-H version 42, please follow these steps:

1. Download the installation package : `git clone https://github.com/SARRA-cropmodels/SARRA-H/`
2. Run the installer file : `SarraH_4_2_setup_Diff2.exe` and follow the installation wizard
3. Copy/paste the interface executable `SarraH_Interface_v42New.exe` into the installation path
4. Run the interface executable `SarraH_Interface_v42New.exe` - running in administrator mode troubleshoots most runtime bugs it the latest Windows versions

## Examples and Scenarios

SARRA-H version 42 includes a comprehensive set of examples in the provided database. These examples showcase different simulation scenarios and can serve as a valuable resource for users.

## Automation and Scripting

For users who need to perform a large number of simulations and wish to automate scenario management, SARRA-H provides the option to integrate the SarraHMoteurv42.exe calculation engine into an automation process using scripting languages such as R. Example files with the required formatting can be found in the SimulAuto directory. 
## Documentation

The following documentation resources are available for reference:

- User Manual [[EN](./docs/SARRA-H_manual_EN.pdf)/[FR](./docs/SARRA-H_manual_FR.pdf)]: Provides detailed instructions on using SARRA-H and its various features. 
- Summary documents:
  - Simulation Scenario Management Overview [[FR](./docs/SARRA-H_simulation_scenarios_FR.pdf)]: Provides an overview of managing simulation scenarios in SARRA-H.
  - Calibration Steps Summary [[FR](./docs/SARRA-H_calibration_procedure_FR.pdf)]: Outlines the steps involved in calibrating new species/variety models or different versions of existing models.
- Training documents:
  - SARRA-H Model Overview [[EN](./docs/SARRA-H_processes_description_EN.pdf)/[FR](./docs/SARRA-H_processes_description_FR.pdf)]: Offers a comprehensive understanding of the SARRA-H model, its underlying principles, and its applications.
  - Workshop for Meteorological Services, Niamey 2013, and Abidjan 2014 [[FR](./docs/SARRA-H_workshops_2013-2014_FR.pdf)]: Provides workshop materials used for training meteorological services on utilizing SARRA-H.

Most documentation mentions previous model version, however instructions are equally suitable for use of version v42.

## Changelog

### SARRA-H v42 (01/04/2021)

- Added a new species: cotton. The model now provides exemple calibration parameters and simulations for millet, sorghum, maize, upland rice, wheat, soybean, and cotton.
- Improved continuous flowering for soybean and cotton to enhance accuracy in the simulation of these crops.
- Enhanced the consideration of vegetal cover effect (mulching) and its degradation to provide more realistic simulation results.
- Incorporated the concentration of CO2 (CC effect) for C4 plants as part of the Agmip-Maïs project.
- Accounted for sowing density in maize based on the AgMip project findings.
- Included different intensification levels based on reference trials and field monitoring conducted in Burkina Faso and Senegal for the Agmip-Maïs project.
- Calibration and validation of new varieties based on controlled experiments
