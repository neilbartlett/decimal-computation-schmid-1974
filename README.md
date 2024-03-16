# decimal-computation-schmid-1974
APL and other artifacts from Schmid, H. Decimal Computation. (Wiley, New York, 1974) ISBN 978-0-471-76180-8

# APL

The apl directory contains APL code from the appendices from the book.

The code runs under Dyalog (tested on 18.2 on MacOs). The code uses the code style from the booka which does not use the dfn standard but rather the older APL style. To get it to run under Dyalog, the code was modified slightly  to use the thorn/format ⍕ which is modern equivalent of DFT. Note DFT was an APL/360 format command -- see https://dl.acm.org/doi/pdf/10.1145/585882.585894 for details.

# Use

Clone the repo and Dyalog RIDE dev environment.

Create a linked namespace to read the code in (this assume a Mac change the slashes correspondingly for windows)
```
      ]LINK.Create decimalcomputation {full-directory-spec-to-local-repo}/decimal-computation-schmid-1974/apl
```
This should reply with
```
Linked: #.decimalcomputation → {full-directory-spec-to-local-repo}/decimal-computation-schmid-1974/apl
```

To check status use
```
      ]LINK.status
 ```
      
Once loaded you can test the APL. The following should Table 7.3 on page 168 of the book.

```
      #.decimalcomputation.COSANDSIN 30
```
The results should be
```
   N.   I.   J.         X.         Y       SUM MU    PRODUCT K. 
    0    0    0    1.000000    0.000000    0.000000    1.000000
    1    0    1    1.000000    1.000000   45.000000    1.414214
    2    1    1    1.100000    0.900000   39.289407    1.421267
    3    1    2    1.190000    0.790000   33.578814    1.428356
    4    1    3    1.269000    0.671000   27.868221    1.435480
    5    1    4    1.201900    0.797900   33.578814    1.442639
    6    1    5    1.281690    0.677710   27.868221    1.449835
    7    1    6    1.213919    0.805879   33.578814    1.457066
    8    1    7    1.294507    0.684487   27.868221    1.464333
    9    1    8    1.226058    0.813938   33.578814    1.471636
   10    1    9    1.307452    0.691332   27.868221    1.478976
   11    2    1    1.300539    0.704406   28.441159    1.479050
   12    2    2    1.293495    0.717412   29.014098    1.479124
   13    2    3    1.286320    0.730347   29.587037    1.479198
   14    2    4    1.279017    0.743210   30.159975    1.479272
   15    2    5    1.286449    0.730420   29.587037    1.479346
   16    2    6    1.279145    0.743284   30.159975    1.479420
   17    2    7    1.286578    0.730493   29.587037    1.479494
   18    2    8    1.279273    0.743359   30.159975    1.479568
   19    2    9    1.286706    0.730566   29.587037    1.479642
   20    3    1    1.285976    0.731853   29.644332    1.479643
   21    3    2    1.285244    0.733139   29.701628    1.479643
   22    3    3    1.284511    0.734424   29.758924    1.479644
   23    3    4    1.283776    0.735708   29.816220    1.479645
   24    3    5    1.283041    0.736992   29.873515    1.479646
   25    3    6    1.282304    0.738275   29.930811    1.479646
   26    3    7    1.281565    0.739558   29.988107    1.479647
   27    3    8    1.280826    0.740839   30.045403    1.479648
   28    3    9    1.281567    0.739558   29.988107    1.479648
   29    4    1    1.281493    0.739686   29.993837    1.479649
   30    4    2    1.281419    0.739815   29.999566    1.479649
COSL=X÷PK=     0.8659791861
ERROR=COSL-X÷PK= ¯0.0000462177248
SINL=Y÷PK.     0.5000800429
ERROR=SINL-Y÷PK= 0.00008004290462
      