GPDMA have a lot of amazing feature
one of them is to send a signal to LPTIM t generate a pulse every time a transfer is complete as a signal
this signal can be used in a lot of ways
here is a simple example that explain how to implement this feature
You can follow DstBuffer and SrcBuffer in live expression and monitor LPTIM CH1 which i think its PB2(check NUCLEO-H563 schematics MB1404) to see a pulse is generated juste when GPDMA complete the transfer  
the key point here is to select the right trigger source which in our ase is :
hlptim1.Init.Trigger.Source = LPTIM_TRIGSOURCE_5;
