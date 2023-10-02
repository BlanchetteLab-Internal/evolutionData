# evolutionData
Many of our lab members use sequence alignment data within the context of evolution. The existing MAF files efficiently stores sequences from different species but using programs to extract orthologous sequences from .maf files can take days to months. I introduce how I preprocessed the orthologous sequence data and where it is saved.

The maf file that contains sequence alignment of mammals and inferred ancestors can be found at
https://repo.cs.mcgill.ca/PUB/blanchem/Boreoeutherian/
Alignment was done using Multiz and ancestral inference was done using Ancestors1.0

The preprocessed version is stored at
/home/mcb/users/dlim63/conservation/data/seqDictPad_chr1.pkl

You can load it using pandas 
* import pandas as pd
* chrom = 1
* alignment = pd.read_pickle(f'/home/mcb/users/dlim63/conservation/data/seqDictPad_chr{chrom}.pkl')

alignment is basically a python dictionary that stores sequences of different species. Keys to this dictionary is the name of the species 
names = ['hg38', 'panTro4','gorGor3', 'ponAbe2', 'nomLeu3', 'rheMac3', 'macFas5', 'papAnu2', 'chlSab2', 'calJac3', 'saiBol1', 'otoGar3', 'tupChi1', 
         'speTri2', 'jacJac1', 'micOch1', 'criGri1', 'mesAur1', 'mm10', 'rn6', 'hetGla2', 'cavPor3','chiLan1', 'octDeg1',
         'oryCun2', 'ochPri3','susScr3','vicPac2','camFer1','turTru2', 'orcOrc1', 'panHod1','bosTau8','oviAri3','capHir1','equCab2','cerSim1','felCat8','canFam3',
          'musFur1','ailMel1', 'odoRosDiv1', 'lepWed1','pteAle1','pteVam1',  'eptFus1', 'myoDav1','myoLuc2','eriEur2',
        'sorAra2', 'conCri1','loxAfr3', 'eleEdw1','triMan1','chrAsi1','echTel2','oryAfe1','dasNov3',
          '_HP', '_HPG', '_HPGP', '_HPGPN', '_RM', '_RMP', '_RMPC', '_HPGPNRMPC', '_CS', '_HPGPNRMPCCS', '_HPGPNRMPCCSO' , '_HPGPNRMPCCSOT',
         '_CM', '_MR', '_MCM', '_MCMMR', '_JMCMMR', '_SJMCMMR', '_CO', '_CCO', '_HCCO', '_SJMCMMRHCCO', '_OO', '_SJMCMMRHCCOOO', '_HPGPNRMPCCSOTSJMCMMRHCCOOO'
        , '_VC', '_TO', '_OC', '_BOC', '_PBOC', '_TOPBOC', '_VCTOPBOC', '_SVCTOPBOC',
          '_EC', '_OL', '_AOL', '_MAOL', '_CMAOL' , '_FCMAOL', '_ECFCMAOL',
          '_PP', '_MM', '_EMM', '_PPEMM', '_ECFCMAOLPPEMM', '_SVCTOPBOCECFCMAOLPPEMM',
          '_SC', '_ESC', '_SVCTOPBOCECFCMAOLPPEMMESC', '_HPGPNRMPCCSOTSJMCMMRHCCOOOSVCTOPBOCECFCMAOLPPEMMESC',
          '_LE', '_LET', '_CE', '_LETCE', '_LETCEO', '_LETCEOD', '_HPGPNRMPCCSOTSJMCMMRHCCOOOSVCTOPBOCECFCMAOLPPEMMESCLETCEOD'
         ]

