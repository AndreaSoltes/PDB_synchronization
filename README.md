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
| 2022-09-28 |      278           |        223             |      885           |         293          |            236           |       |
| 2022-10-05 |      236           |        338             |      915           |         250          |            361           |       |
| 2022-10-16 |      449           |        213             |      711           |         458          |            238           |       |
| 2022-10-19 |      189           |        167             |      693           |         214          |            211           |       |
| 2022-10-26 |      182           |        401             |      695           |         200          |            411           |       |
| 2022-11-04 |      519           |        285             |      709           |         534          |            290           |       |
| 2022-11-09 |      324           |        196             |      838           |         336          |            216           |       |
| 2022-11-16 |      303           |        190             |      821           |         318          |            210           |       |
| 2022-11-23 |      295           |        346             |      851           |         364          |            374           |       |
| 2022-11-30 |      174           |        452             |      832           |         220          |            492           |       |
| 2022-12-07 |      236           |        286             |      1002          |         251          |            358           |       |
| 2022-12-14 |      265           |        214             |      1172          |         279          |            226           |       |
| 2022-12-21 |      217           |        697             |      956           |                   |                       |       |

## Lists of New/Changed PDB files/New Sequences

[lists_2022-07-21.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257025/lists_2022-07-21.zip)

[lists_2022-07-27.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257029/lists_2022-07-27.zip)

[lists_2022-08-03.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9257035/lists_2022-08-03.zip)

[lists_2022-08-10.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9299993/lists_2022-08-10.zip)

[lists_2022-08-17.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9358405/lists_2022-08-17.zip)

[lists_2022-08-24.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9417466/lists_2022-08-24.zip)

[lists_2022-08-31.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9460556/lists_2022-08-31.zip)

[lists_2022-09-07.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9504637/lists_2022-09-07.zip)

[lists_2022-09-14.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9565258/lists_2022-09-14.zip)

[lists_2022-09-21.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9615272/lists_2022-09-21.zip)

[lists_2022-09-28.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9664593/lists_2022-09-28.zip)

[lists_2022-10-05.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9717403/lists_2022-10-05.zip)

[lists_2022-10-16.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9800182/lists_2022-10-16.zip)

[lists_2022-10-19.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9818600/lists_2022-10-19.zip)

[lists_2022-10-26.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9868397/lists_2022-10-26.zip)

[lists_2022-11-04.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9939132/lists_2022-11-04.zip)

[lists_2022-11-09.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/9981071/lists_2022-11-09.zip)

[lists_2022-11-16.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10040108/lists_2022-11-16.zip)

[lists_2022-11-23.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10115992/lists_2022-11-23.zip)

[lists_2022-11-30.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10165709/lists_2022-11-30.zip)

[lists_2022-12-07.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10183436/lists_2022-12-07.zip)

[lists_2022-12-14.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10229629/lists_2022-12-14.zip)

[lists_2022-12-21.zip](https://github.com/AndreaSoltes/PDB_synchronization/files/10276554/lists_2022-12-21.zip)

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

## Synchronizing MMCIF database

`rsync -rlpt -avic -z --delete rsync.ebi.ac.uk::pub/databases/pdb/data/structures/divided/mmCIF/ ./mmCIF > download-mmcif-$(date +%F).log`
