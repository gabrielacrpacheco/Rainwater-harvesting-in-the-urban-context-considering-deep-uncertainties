# Rainwater-harvesting-in-the-urban-context-considering-deep-uncertainties
To evaluate the different policies for implementing Rainwater Harvesting Systems (RWHS) considering deep uncertainties, the code that assesses the impacts of the RWHS for users has been extended to evaluate the effects on the utility.
It was developed in my PhD at UnB.
The program considers the following steps, which are divided into codes:

CODE 1: 1000 rainfall regime scenarios are created using bootstrapping analysis;
  - Input data: csv file of a historical rainfall series;
   
CODE 2: 1000 scenarios of deep uncertainty parameters - DUs (households users, discount rate, tariff and operating costs) are created using the LHS method;
  - Input data: minimum and maximum limits for each DU;
    
CODE 3: Based on the input data, rainwater harvesting systems are evaluated through technical and economic indicators in the context of uncertainties for the users and the utility.
  - Input data:
      File of 1000 rainfall regime scenarios (Code 1);
      Files of 1000 scenarios of deep uncertainty parameters (Code 2);
      File with demand, number and characteristics of households, tank volume for each type of household, tank prices, tariff structure, cost per volume for the utility, sizing and economic parameters (csv format).
  - Continuous simulation of the daily mass balance for the different categories of households;
  - Calculation of consumption (per month, per type of household and per year of the life span);
      Calculation of consumption of rainwater for each different household in the city and for all of them;
      Calculation of consumption if rainwater harvesting were not implemented for each different household in the city and for all of them;
      Determination of consumption indicators;
          For the utility: WS (percentage of water saved);
          For users: SD (satisfied demand), REL (reliability of the systems), RH (percentage of rainwater harvested);
  - Economic Evaluation (with and without rainwater harvesting);
      Determination of the amount paid per type of household and for all of them (utility revenue);
      Determination of the utility expenses for producing the consumed water volume per type of household and for all of them (utility expense);
      Determination of economic indicators;
          For the utility: BCR (benefit cost rate), BCM (benefit cost rate modified);
          For users: BCR (benefit cost rate), NPV (net present value), NPVV (net present value per volume of rainwater consumed)
