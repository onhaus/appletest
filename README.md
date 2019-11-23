# appletest
Quick script to read configuration, test, and diagnose Apple computers using Apple's own Terminal Commands.
Saves file 'system_report.txt' to current Desktop.

Creates a bin file to run local tests on a macbook, macbookpro, imac, or mac mini.
1.  Current Configuration Information
1A. HARDWARE OVERVIEW 
    Outputs to file (system_profiler SPHardwareDataType > ~/Desktop/system_report.txt)
    Returns the following example:
      Model Name: MacBook Pro
      Model Identifier: MacBookPro15,2
      Processor Name: Quad-Core Intel Core i7
      Processor Speed: 2.7 GHz
      Number of Processors: 1
      Total Number of Cores: 4
      L2 Cache (per Core): 256 KB
      L3 Cache: 8 MB
      Hyper-Threading Technology: Enabled
      Memory: 16 GB
      Boot ROM Version: 1037.40.124.0.0 (iBridge: 17.16.11081.0.0,0)
      Serial Number (system): xxxxxxxxxxxxxxx
      Hardware UUID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
      Activation Lock Status: Enabled
 1B.  DIAGNOSTICS
      Appends file (system_profiler SPDiagnosticsDataType >> ~/Desktop/system_report.txt)
      Returns the following example:
      Diagnostics:
        Power On Self-Test:
          Last Run: 11/19/19, 5:17 PM
          Result: Passed
 1C.  PING 
      ping -ac 10 8.8.8.8 >> ~/Desktop/system_report.txt
