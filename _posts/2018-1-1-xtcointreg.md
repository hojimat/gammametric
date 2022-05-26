---
layout: post
title: Panel FMOLS/DOLS command for Stata
lang: english
categ: codes
keywords: stata, cointreg, pedroni, panel data
tags: economics
---
[Pedroni's 1996 paper](https://econpapers.repec.org/article/tprrestat/v_3a83_3ay_3a2001_3ai_3a4_3ap_3a727-731.htm) models panel FMOLS estimators as a simple average between each panel's FMOLS for coefficients and sum divided by the square root of the total number of panels for t-statistics.  

There already exists a tool for time series FMOLS estimation called `cointreg` written by [Qunyong Wang and Na Wu](http://ageconsearch.umn.edu/bitstream/229441/2/sjart_st0272.pdf).

Meet a new command for Stata `xtcointreg` that  applies group mean averaging to it.

You need to [install `cointreg` first](http://ageconsearch.umn.edu/bitstream/229441/2/sjart_st0272.pdf). The documentation is the same as `cointreg` plus one option `full`. The package can be installed using `ssc install xtcointreg`.  

**Update:** If you have installed the program successfully but it is not working for some reason, please try this workaround:  
1. write a command `which xtcointreg` and find the location of the **xtcointreg.ado** file;
2. open that file with any text editor and remove the line number 8 `capt program drop xtcointreg`;
3. save the file and try to run `xtcointreg` again. This problem is related to the publisher of the code and not to my code itself.
