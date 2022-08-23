# PDB_synchronization
Daily progress of PDB synchronization

|    Date    | Number of New PDB files | Number of Changed PDB files | Number of New Sequences |                       Notes                      |
|:----------:|:-----------------------:|:---------------------------:|:-----------------------:|:------------------------------------------------:|
| 2022-07-21 |           1220          |             738             |           2273          |     Synchronization from 2022-06-26              |
| 2022-07-22 |            0            |              0              |            0            |                                                  |
| 2022-07-23 |            0            |              0              |            0            |                                                  |
| 2022-07-24 |            0            |              0              |            0            |                                                  |
| 2022-07-25 |            0            |              0              |            0            |                                                  |
| 2022-07-26 |            0            |              0              |            0            |                                                  |
| 2022-07-27 |           259           |             247             |           749           |                                                  |
| 2022-07-28 |            0            |              0              |            0            |           Problem with synchronization!          |
| 2022-07-29 |            0            |              0              |            0            |                                                  |
| 2022-07-30 |            0            |              0              |            0            |                                                  |
| 2022-07-31 |            0            |              0              |            0            |                                                  |
| 2022-08-01 |            0            |              0              |            0            |                                                  |
| 2022-08-02 |            -            |              -              |            -            |           Problem with synchronization!          |
| 2022-08-03 |           274           |             232             |           710           |           Problem with synchronization!          |
| 2022-08-04 |            0            |              0              |            0            |                                                  |
| 2022-08-05 |            0            |              0              |            0            |                                                  |
| 2022-08-06 |            0            |              0              |            0            |                                                  |
| 2022-08-07 |            0            |              0              |            0            |                                                  |
| 2022-08-08 |            0            |              0              |            0            |                                                  |
| 2022-08-09 |            0            |              0              |            0            |                                                  |
| 2022-08-10 |           227           |             230             |           734           |                                                  |
| 2022-08-11 |            0            |              0              |            0            |                                                  |
| 2022-08-12 |            0            |              0              |            0            |                                                  |
| 2022-08-13 |            0            |              0              |            0            |                                                  |
| 2022-08-14 |            0            |              0              |            0            |                                                  |
| 2022-08-15 |            0            |              0              |            0            |                                                  |
| 2022-08-16 |            0            |              0              |            0            |                                                  |
| 2022-08-17 |           238           |             241             |           676           |                                                  |
| 2022-08-18 |            0            |              0              |            0            |                                                  |
| 2022-08-19 |            0            |              0              |            0            |                                                  |
| 2022-08-20 |            0            |              0              |            0            |                                                  |
| 2022-08-21 |            0            |              0              |            0            |                                                  |
| 2022-08-22 |            0            |              0              |            0            |                                                  |
| 2022-08-23 |            0            |              0              |            0            |                                                  |

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

