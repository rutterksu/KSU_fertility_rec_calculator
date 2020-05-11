# KSU fertility calculator

__Name:__ Bryan Rutter  
__Semester:__ Spring 2020  
__Project Area:__ Soil Fertility/Agronomy  

## Objective:

Create function(s) that automate the calculation of lime and fertilizer application rates based on soil test results from the KSRE Soil Testing Laboratory.

## Rationale:

Fertilizer amendments are often required to correct nutrient deficiencies in agricultural production systems. Over-fertilization increases the risk of eutrophication of surface water, while under-fertilization can lead to reduced crop yield, quality, and farm profitability. Fertilizer application rates are often based on a yield goal or an in-season estimate of crop yield potential, but should be guided by soil tests to improve their accuracy when possible. However, these calculations may involve several variables and can be cumbersome to calculate by hand. The KSRE Soil Testing Lab provides soil testing services and fertilizer recommendations to Kansas homeowners and producers. Fertilizer recommendations are reported via PDF and excel documents which are computed and compiled by proprietary third-party software. The equations used to calculate fertilizer application rates are freely available, but the third party software can often be a _black box_ and may be difficult for lab employees to troubleshoot. Creating a Python program to automate these calculations could serve as a validation and troubleshooting tool for lab workers, and make it easier to communicate potential problems with the STRS software developers.

# Function inputs

Input data consists of a combination of user inputs and soil measurements. Soil measurements include soil pH, buffer pH, soil organic matter, and plant available-P, -K, and -N, and must be imported as a csv file generated by the lab's data management system. Context parameters including tillage practice, crop type, yield goal, and sampling depth are also required. Equations used to compute fertilizer application rates are sourced from the [KSU Fact Sheet MF-2586](https://bookstore.ksre.ksu.edu/pubs/mf2586.pdf). 

Note 1: Recent changes to the STRS software allow for tillage, crop type, yield goal, and sampling depth to be exported with soil test data directly by STRS. The only user input required is whether to save the output or not.

# Function input variable descriptions
__OrderNo__: The order number for a particular customer's samples. Used for lab reference only.  
__LabNo__: The lab number assigned to each soil sample. Used for lab reference only.  
__Crop__: String or factor indicating the intended crop to be grown (e.g. "Corn", "Soybeans", etc.)  
__YieldGoal__: Numeric value providing an estimation of average yield potential of the intended for the specific field   
__Tillage__: String or factor indicating what tillage management practices are employed  
__PrevCrop__: String or factor indicating the previously grown crop. Used to adjust N-rate calculations  
__OM__: Numeric value representing the soil organic matter concentration of the soil (%). Required for N-rate calculations  
__NO3__: Numeric value representing the KCl extractable nitrate content of the soil (ppm or mg kg^-1^). Required for N-rate calculations  
__P__: Numeric value representing the concentration of Bray-1 or Mehlich-3 extractable P in the soil (ppm or mg kg^-1^). Required for P fertilizer rate calculations  
__K__: Numeric value representing the concentration of ammonium acetate or Mehlich-3 extractable K in the soil (ppm or mg kg^-1^). Required for K fertilizer rate calculations    
__pH__: Numeric value representing the pH of the soil  
__BUFpH__: Numeric value representing the Sikora buffer pH of the soil  

Soil test data are collected by the KSRE Soil Testing Lab in accordance with the [Recommended Soil Test Procedures for the North Central Region](https://extensiondata.missouri.edu/pub/pdf/specialb/sb1001.pdf)

# Function output variable descriptions

__OrderNo__: The order number for a particular customer's samples. Used for lab reference only.  
__LabNo__: The lab number assigned to each soil sample. Used for lab reference only.  
__Crop__: The intended crop to be grown (e.g. "Corn", "Soybeans", etc.)  
__LimeApp__: Lime application rate as computed by STRS (lbs 100% ECCE aglime ac<sup>-1</sup>)  
__Lime_rec_KSU__: Lime application rate according to MF-2586 (lbs 100% ECCE aglime ac<sup>-1</sup>)  
__NApp1__: Nitrogen application rate computed by STRS (lbs N ac<sup>-1</sup>)  
__N_KSU_Rec__: Nitrogen application rate according to MF-2586 (lbs P2O5 ac<sup>-1</sup>)  
__P2O5App__: Phosphorus application rate computed by STRS (lbs P2O5 ac<sup>-1</sup>)  
__P2O5_Rec_KSU__: Phosphorus application rate according to MF-2586 (lbs P2O5 ac<sup>-1</sup>)  
__K2OApp__: Potassium application rate computed by STRS (lbs K2O ac<sup>-1</sup>)  
__K2O_Rec_KSU__: Potassium application rate according to MF-2586 (lbs K2O ac<sup>-1</sup>)  

## Sketch
<img src="Project_schematic.png" alt="workflow" width="750"/>

## References

Agronomy Department, Kansas State University (2015). _Soil Test Inerpretations and Fertilizer Recommendations (MF-2586)_. Retrieved from https://bookstore.ksre.ksu.edu/pubs/mf2586.pdf

Missouri Agricultural Experiment Station SB 1001 (2015). _Recommended Chemical Soil Test Procedures for the North Central Region (NCERA No. 221-Revised)_. Retrieved from https://extensiondata.missouri.edu/pub/pdf/specialb/sb1001.pdf