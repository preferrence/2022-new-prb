startParseToEnd --> parseToEnd // FFT
                    parseToEndAllNoPro //other
                        --> partitionTask -->   expandAST2ThreadISONums --> loopUnrolledByUndevisableGroup
                        --> eliminateIfStmt --> getSubTaskNum -->   genAccCodeNoISOCal --> generateISOTBGroupForFISC
                        --> orderSPMKernel  --> spmDataReuse_modifyBaseAddr //or
                                            --> reductionSplited_modifyBaseAddr// or
                                            --> allKernel_modifyBaseAddr --> modify_subkernel_dir_name -->testDataGenerate

genAccCodeNoISOCal --> analysisLoopBound --> preCalStmtVal --> analysisStmt --> initSubTaskInstanceNum
    --> analysisDataRegionClassicTB --> initSPMInfo -->  modifyArrayRef2SPMArray --> dealAllArrayRefExpr_lin_base_spmaddr 
    --> dealAllArrayRefExpr_lin --> getArraySubscriptExprAddr_spm


analysisDataRegionClassicTB --> transCooFromBlock2Grid --> findThreadISOGroupNums --> analysisDataRegionForClassicEB

analysisDataRegionForClassicEB --> getAllArrayRef --> (init the data region) --> (cal low bound) 
                                                                             --> getArraySubStmt -> calArraySubStmtVal
                                                                             --> (cal the up bound) -- (get gap)


getArraySubscriptExprAddr_spm -->  getArraySubStmt -->  calArraySubStmtVal -- (increase dim) -- (transpose) -- (minus data region for spm addr) -- (get line addr)  --- 输出spm线性地址