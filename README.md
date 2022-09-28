# PDB_synchronization
Weekly progress of PDB synchronization

|    Date    | # of New PDB files | # of Changed PDB files | # of New Sequences | # of New MMCIF files | # of Changed MMCIF files | Notes |
|:----------:|:------------------:|:----------------------:|:------------------:|:--------------------:|:------------------------:|:-----:|
| 2022-07-21 |      1220          |        738             |      2273          |                      |                          |       |
| 2022-07-27 |      259           |        247             |      749           |                      |                          |       |
| 2022-08-03 |      274           |        232             |      710           |                      |                          |       |
| 2022-08-10 |      227           |        230             |      734           |                      |                          |       |
| 2022-08-17 |      238           |        241             |      676           |                      |                          |       |
| 2022-08-24 |      279           |        713             |      855           |                      |                          |       |
| 2022-08-31 |      253           |        153             |      661           |                      |                          |       |
| 2022-09-07 |      254           |        232             |      613           |                      |                          |       |
| 2022-09-14 |      227           |        266             |      719           |                      |                          |       |
| 2022-09-21 |      224           |        157             |      619           |         240          |            176           | Download:2022-09-16 |
| 2022-09-28 |      278           |        223             |      885           |                   |                       |  |

## Lists of New/Changed PDB files/New Sequences

### 2022-07-21

[lists_2022-07-21.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257025/lists_2022-07-21.zip)

### 2022-07-27

[lists_2022-07-27.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257029/lists_2022-07-27.zip)

## 2022-08-03

[lists_2022-08-03.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257035/lists_2022-08-03.zip)

## 2022-08-10

[lists_2022-08-10.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9299993/lists_2022-08-10.zip)

## 2022-08-17

[lists_2022-08-17.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9358405/lists_2022-08-17.zip)

## 2022-08-24

[lists_2022-08-24.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9417466/lists_2022-08-24.zip)

## 2022-08-31

[lists_2022-08-31.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9460556/lists_2022-08-31.zip)

## 2022-09-07

[lists_2022-09-07.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9504637/lists_2022-09-07.zip)

## 2022-09-14

[lists_2022-09-14.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9565258/lists_2022-09-14.zip)

## 2022-09-21

[lists_2022-09-21.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9615272/lists_2022-09-21.zip)

## 2022-09-28

[lists_2022-09-28.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9664593/lists_2022-09-28.zip)

# Synchronizing PDB database

`rsync -rlpt -avic -z --delete rsync.ebi.ac.uk::pub/databases/pdb/data/structures/divided/pdb/ ./pdb > download-pdb-$(date +%F).log`

## Number of New PDB files

`grep -c ">f+" download-pdb-$(date +%F).log`

## Number of Changed PDB files

`grep -c ">fc.t" download-pdb-$(date +%F).log`

# Extract FASTA files

`./prank analyze fasta-masked datasets/pdb-$(date +%F).ds -o datasets/fastas-$(date +%F)/ &> datasets/fastas-$(date +%F).log`

## Generate chunks of New Sequences

`../../generate_chunks_actual.py > chunks-$(date +%F).log`

## Number of New Sequences

`grep -c "New sequence" chunks-$(date +%F).log`

