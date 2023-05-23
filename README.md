# evolutionData
Many of our lab members use sequence alignment data within the context of evolution. The existing MAF files efficiently stores sequences from different species but using programs to extract orthologous sequences from .maf files can take days to months. I introduce how I preprocessed the ortholoous sequence data and where it is saved.

The maf file that contains sequence alignment of mammals and inferred ancestors can be found at
https://repo.cs.mcgill.ca/PUB/blanchem/Boreoeutherian/
Alignment was done using Multiz and ancestral inference was done using Ancestors1.0

The preprocessed version is stored at
/home/mcb/users/dlim63/conservation/data/seqDictPad_chr1.pkl

You can load it using pandas 
import pandas as pd
chrom = 1
alignment = pd.read_pickle(f'/home/mcb/users/dlim63/conservation/data/seqDictPad_chr{chrom}.pkl')
