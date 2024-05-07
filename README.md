# Rainwater-harvesting-in-the-urban-context-considering-deep-uncertainties
This code assesses the effects on both the utility and the users of implementing rainwater harvesting systems for a city, considering deep uncertainties.
It was developed in my PhD at UnB.

The program considers the following steps, which are divided into codes:

Code 1: 1000 rainfall regime scenarios are created using bootstrapping analysis;
  - Input data: csv file of a historical rainfall series;
   
Code 2: 1000 scenarios of deep uncertainty parameters - DUs (households users, discount rate, tariff and operating costs) are created using the LHS method;
  - Input data: minimum and maximum limits for each DU;
    
Code 3: Based on the input data, rainwater harvesting systems are evaluated through technical and economic indicators in the context of uncertainties for the users and the utility.
  - Input data: input files generated with codes 1 and 2, files with demand information, reservation prices, tariff structure, sizing and economic parameters.
  - Continuous simulation of the daily mass balance for each storage volume defined as input;
Determination of SD, CON, RH and determination of the ideal volume;
Economic evaluation;
Determination of NPV, NPVV and BCR;
Determination of the volume that presents the maximum value of each indicator as well as the other indicators for each volume.

  - Code 4: Drawing of parallel coordinates plot with indicators calculated for all scenarios (total or for each demand value).
      Input data: csv file with the results presented by code 4 for all demand values.
    
  - Code 5: Drawing of scatter plot with Satisfied Demand (SD) indicator by the factors of DUs and hydrological parameters.
      Input data: csv file with the results presented by code 4 for all demand values.



