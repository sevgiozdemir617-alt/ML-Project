# Data

The project uses World Bank World Development Indicators data.

## Source

World Bank WDI: https://datatopics.worldbank.org/world-development-indicators/

## Data policy

- Keep raw downloads unchanged in `data/raw/` if they are committed.
- Document the download date and selected indicator codes.
- Do not commit credentials or private data.
- The final modelling table should be created reproducibly from the raw source or API.

## Selected indicator codes

```text
NY.GDP.MKTP.KD.ZG  GDP growth (annual %)
NY.GDP.PCAP.KD     GDP per capita (constant 2015 US$)
FP.CPI.TOTL.ZG     Inflation, consumer prices (annual %)
NE.GDI.FTOT.ZS     Gross fixed capital formation (% of GDP)
SL.UEM.TOTL.ZS     Unemployment, total (% of total labour force)
NE.EXP.GNFS.ZS     Exports of goods and services (% of GDP)
NE.IMP.GNFS.ZS     Imports of goods and services (% of GDP)
BX.KLT.DINV.WD.GD.ZS  FDI net inflows (% of GDP)
NE.CON.GOVT.ZS     General government final consumption expenditure (% of GDP)
SP.POP.GROW       Population growth (annual %)
```
