# KSU fertility calculator

## Objective:

Create function(s) that automate the calculation of lime and fertilizer application rates based on soil test results from the KSRE Soil Testing Laboratory.

## Rationale:

Fertilizer ammendments are often required to correct nutrient deficiencies in agricultural production systems. Over-fertilization increases the risk of eutrophication of surface water, while under-fertilization can lead to reduced crop yield, quality, and farm profitability. Fertilizer application rates are often based on a yield goal or in-season estimate of yield potential, but should be guided by soil tests to improve their accuracy when possible. However, these calculations may involve several variables and may be cumbersome to calculate by hand. The KSRE Soil Testing Lab provides soil testing services and fertilizer recommendations to Kansas homeowners and producers. Fertilizer recommendations are reported via PDF and excel documents which are computed and compiled by proprietary third-party software. The equations used to calculate fertilizer application rates are freely available to the public, but third party software can often be a _black box_ and may be difficult to troubleshoot. Creating a Python program to automate these calculations could serve as a useful validation tool and improve the transparency of how application rates are determined.

## Sketch
<img src="Project_schematic.png" alt="workflow" width="750"/>

## References

__MF-2586__: _Soil Test Inerpretations and Fertilizer Recommendations_, 2018, Department of Agronomy, Kansas State University