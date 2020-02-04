# Semester project

## Objective:

Create function(s) to automate the calculation of lime and fertilizer application rates based on soil test results from the KSRE Soil Testing Laboratory.

## Rationale:

Fertilizer ammendments are often required to correct nutrient deficiencies in agricultural production systems. Over-fertilization increases the risk of eutrophication of surface water, while under-fertilization can lead to reduced crop yield, quality, and farm profitability. Fertilizer application rates should be determined guided by soil tests when possible to improve their accuracy. However, these calculations may involve several variables and may be cumbersome to calculate by hand. The KSRE Soil Testing Lab provides soil testing services and fertilizer recommendations to Kansas homeowners and producers. Fertilizer recommendations are reported via PDF and excel documents compiled by proprietary third-party software. The equations used to calculate fertilizer application rates are freely available to the public, but the software used by the lab is a "black box" in some ways. Current tools used by the lab to validate our recommended application rates largely involve copy/pasting soil test values into an excel-based calculator or hand calculation. This process can be tedious and prone to transcription errors. Automating this process could improve the workflow of the lab and make it easier to diagnose problems in the third-party software.

## Outcomes

I would like the functions to produce an xlsx file with 8 columns lime_rate, delta_lime, N_rate, delta_N, P2O5_rate, delta_P2O5, K2O_rate, delta_K2O

## Sketch
<img src="./semester_project/Project_schematic.png" alt="workflow" width="750"/>

## References

__MF-2586__: _Soil Test Inerpretations and Fertilizer Recommendations_