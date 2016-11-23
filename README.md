Description: B3 - Delta PLC program
#fix Timesync error
Bug:
+ Delta PLC RTC  - Day Register(x01):
  - 1 ~ 7 (Mon ~ Sun)
+ Kinco HMI RTC - Day Register(x06):
  - 0 ~ 6 (Sun ~ Sat)

Means that in HMI, Sunday is 0 but in PLC, Sunday is 7. That cause bug that cannot excute TWR function
Fix:
+ If Day is 0 then change to 7 ^^, after that excute TWR function

