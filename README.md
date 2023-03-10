# Topsis_Jashan_102017034

_for: **TOPSIS PACKAGE**_
_submitted by: **Jashanveer Kaur Dhillon**_
_Roll no: **102017034**_
_Group: **CS2**_


Topsis_Jashan_102017034 is a Python library for dealing with Multiple Criteria Decision Making(MCDM) problems.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install Topsis-Jashan-102017034.

```bash
pip install Topsis_Jashan_102017034
```

## Usage

Firstly, install the Topsis_Jashan_102017034 package. After installation of the package, write the following command :-
```
from Topsis_Jashan_102017034.Topsis import topsis
```
topsis() function has four parameters ; The first parameter is for the input csv file , the second parameter is for weights , next parameter is for impacts and the last parameter is for the output csv file.

Example :-
topsis(input.csv,"1,1,1,1","+,-,+,+",output.csv)

Make sure that number of weights and impact is equal to the number of columns in input.csv

You can also run topsis from command line as follows :-
$ python [package name] [path of csv as string] [list of weights as string] [list of sign as string] [path of output file csv]



## Example

#### sample.csv

A csv file showing data for different mobile handsets having varying features.

| Model  | Storage space(in gb) | Camera(in MP)| Price(in $)  | Looks(out of 5) |
| :----: |:--------------------:|:------------:|:------------:|:---------------:|
| M1 | 16 | 12 | 250 | 5 |
| M2 | 16 | 8  | 200 | 3 |
| M3 | 32 | 16 | 300 | 4 |
| M4 | 32 | 8  | 275 | 4 |
| M5 | 16 | 16 | 225 | 2 |

weights vector = [ 1 , 1 , 1 , 1 ]

impacts vector = [ "+" , "+" , "-" , "+" ]

### input:

```python
topsis(input.csv,weights,impacts,result.csv)
```

### output:
```
      TOPSIS RESULTS
-----------------------------

    P-Score  Rank
1  0.534277     3
2  0.308368     5
3  0.691632     1
4  0.534737     2
5  0.401046     4

``` 

## Other notes
* Make sure the csv does not contain categorical values


## License
[MIT](https://choosealicense.com/licenses/mit/)