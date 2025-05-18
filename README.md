# Investment Simulator in Excel

## Language 

  - Procv
  - VF
  - Conditional Formatting
  - Cell Naming

Spreadsheet 1 – Investment Simulator
Investment calculations
=salary*10% (D17)
Calculates 10% of the salary as a suggested monthly contribution.

=FV(D23,D22*12,D21*-1) (D24)
Uses the FV (future value) function to calculate the accumulated amount of an investment:

D23: annual interest rate

D22*12: total number of periods (years converted to months)

D21*-1: monthly contribution amount (negative because it is a payment)

=D24*txrendimento (D25)
Estimates the return obtained on the final value of the investment.

Simulation by age
Lines C29 to C33 and D29 to D33:
Each line simulates the accumulated value up to different ages using:

=FV(D$23,Axx*12,D$21*-1): future value according to age in column A.

=Cxx*txrendimento: estimated return for the calculated future value.

Fund Comparison
=contribution (D37)
Refers to a value defined as a named variable.

=VLOOKUP($D$36&"-"&Bxx,Sheet2!$A$2:$D$19,4,FALSE) (C40 to C45)
Searches for the profitability of different funds based on category and type, concatenating both as the search key.

=$D$37*Cxx (D40 to D45)
Calculates the estimated return by multiplying the contribution by the profitability obtained from the VLOOKUP formula.

=SUM(D40:D45) (D46)
Adds all fund returns to get the estimated total.
challenges for excel course

Spreadsheet2 – Fund Database
Preparing the Search Key
=B2&"-"&C2 to =B19&"-"&C19 (A2 to A19)
Creates a unique key by concatenating the fund category and type (e.g.: “Fixed Income-Conservative”).

Query
=VLOOKUP(G3,$A:$D,4,FALSE) (H3)
Performs a query to retrieve the profitability of a specific fund based on the key entered in G3.
![Planilha](https://github.com/user-attachments/assets/e01d2e4b-a03d-4fd0-8340-04f9bae6bd7e)

[Projeto DIO 1.xlsx](https://github.com/user-attachments/files/20273014/Projeto.DIO.1.xlsx)


