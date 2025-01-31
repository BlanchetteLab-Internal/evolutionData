```markdown
# Evolution Data: Preprocessed Orthologous Sequence Alignment

This repository contains preprocessed mammalian sequence alignment data with ancestral reconstructions for efficient access in evolutionary studies. The original MAF files have been optimized to significantly reduce sequence extraction time from days/months to minutes.

## Data Source
**Original MAF Files**  
Hosted at:  
https://repo.cs.mcgill.ca/PUB/blanchem/Boreoeutherian/  

- Alignment performed with **Multiz**
- Ancestral inference using **Ancestors 1.0**

## Preprocessed Data
**Location**  
`/home/mcb/users/dlim63/conservation/data/seqDictPad_chr1.pkl`

**Format**  
A Pandas-compatible pickle file containing a dictionary structure with padded sequences.

## Usage
```python
import pandas as pd

# Load alignment data for chromosome 1
chrom = 1
alignment = pd.read_pickle(f'/home/mcb/users/dlim63/conservation/data/seqDictPad_chr{chrom}.pkl')

# Access sequences using species keys
human_seq = alignment['hg38']
chimp_seq = alignment['panTro4']
```

## Data Structure
The alignment dictionary contains orthologous sequences with:
- **Keys**: Species identifiers (see full list below)
- **Values**: Corresponding aligned nucleotide sequences

## Species List (Dictionary Keys)
The dataset includes 83 extant species and reconstructed ancestors:

### Extant Species
```
hg38, panTro4, gorGor3, ponAbe2, nomLeu3, rheMac3, macFas5, papAnu2, chlSab2, 
calJac3, saiBol1, otoGar3, tupChi1, speTri2, jacJac1, micOch1, criGri1, 
mesAur1, mm10, rn6, hetGla2, cavPor3, chiLan1, octDeg1, oryCun2, ochPri3,
susScr3, vicPac2, camFer1, turTru2, orcOrc1, panHod1, bosTau8, oviAri3,
capHir1, equCab2, cerSim1, felCat8, canFam3, musFur1, ailMel1, odoRosDiv1,
lepWed1, pteAle1, pteVam1, eptFus1, myoDav1, myoLuc2, eriEur2, sorAra2,
conCri1, loxAfr3, eleEdw1, triMan1, chrAsi1, echTel2, oryAfe1, dasNov3
```

### Reconstructed Ancestors
```
_HP, _HPG, _HPGP, _HPGPN, _RM, _RMP, _RMPC, _HPGPNRMPC, _CS, _HPGPNRMPCCS,
_HPGPNRMPCCSO, _HPGPNRMPCCSOT, _CM, _MR, _MCM, _MCMMR, _JMCMMR, _SJMCMMR,
_CO, _CCO, _HCCO, _SJMCMMRHCCO, _OO, _SJMCMMRHCCOOO, _HPGPNRMPCCSOTSJMCMMRHCCOOO,
_VC, _TO, _OC, _BOC, _PBOC, _TOPBOC, _VCTOPBOC, _SVCTOPBOC, _EC, _OL, _AOL,
_MAOL, _CMAOL, _FCMAOL, _ECFCMAOL, _PP, _MM, _EMM, _PPEMM, _ECFCMAOLPPEMM,
_SVCTOPBOCECFCMAOLPPEMM, _SC, _ESC, _SVCTOPBOCECFCMAOLPPEMMESC,
_HPGPNRMPCCSOTSJMCMMRHCCOOOSVCTOPBOCECFCMAOLPPEMMESC, _LE, _LET, _CE, _LETCE,
_LETCEO, _LETCEOD, _HPGPNRMPCCSOTSJMCMMRHCCOOOSVCTOPBOCECFCMAOLPPEMMESCLETCEOD
```

## Notes
1. Ancestral nodes are prefixed with underscores (e.g., `_HP`)
2. Chromosome 1 data is currently available
3. Sequence data is padded to maintain alignment positions
4. Requires Python pandas package for data loading
```

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

