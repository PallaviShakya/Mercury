# Mercury
Using mercury (https://github.com/marbl/merqury) to assess pacbio hifi reads 


## Create conda env with yml file

```
conda create --name merc --file merqury.yml
```

## Activate the conda env

```
conda activate merc
```

## Get meryl and mercury
```
wget https://github.com/marbl/meryl/releases/download/v1.0/meryl-1.0.Linux-amd64.tar.xz
tar -xf meryl-1.0.Linux-amd64.tar.xz
export PATH=$PWD/meryl-1.0/Linux-amd64/bin:$PATH

git clone https://github.com/marbl/merqury.git
export MERQURY=$PWD/merqury
ln -s $MERQURY/merqury.sh
```
## Run 
```
meryl count k=21 ~/m64069_220815_155249.hifi_reads.fasta output pacbio.meryl

/merqury.sh pacbio.meryl ~/hapla.asm.hap1.p_ctg.fa ~/hapla.asm.hap2.p_ctg.fa ~/M_hapla_assembly_v1.fasta all_assembly_merqury
```
