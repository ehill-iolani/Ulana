# Ulana
***U***nicellular ***L***ong-read ***A***ssembly a***N***d ***A***nnotation

A bacterial genome assembly and annotation pipeline using Fast, HAC or SUP ONT basecalled data from MinION and Flongle flow cells.

ulana

1. vt. To plait, weave, knit, braid; plaiting, weaving. Also unala, nala, unana. Mea ulana ʻia, plaited or woven material, textile. Mea ulana lole, weaver (Isa. 38.12), loom. (PPN langa.)

```
 _   _ _
| | | | | __ _ _ __   __ _
| | | | |/ _` | '_ \ / _` |
| |_| | | (_| | | | | (_| |
 \___/|_|\__,_|_| |_|\__,_|


Ulana v1.0.1

Bacterial genome assembly and annotation
pipeline using Fast, HAC, or SUP ONT basecalled
data from MinION and Flongle flow cells

Usage: /usr/bin/ulana
  -h    help (prints this message)
  -v    version
  -q    minimum quality score; default is 10
  -l    minimum read length; default is 1000
  -c    number of cores to use; default is 4
  -i    name of input fastq file containing reads
  -b    type of basecalling used; the options are: r941_min_fast_g507, r941_min_hac_g507, r941_min_sup_g507
```

# Installation

Docker image to run this pipeline as a container:
```
docker pull ethill/ulana:latest
docker exec -it container_name bash
```

# Sample commands
Fast basecalling
```
ulana -q 8 -l 1500 -c 56 -i fast_basecalled_reads.fastq -b r941_min_fast_g507
```
HAC basecalling
```
ulana -q 9 -l 1500 -c 56 -i hac_basecalled_reads.fastq -b r941_min_hac_g507
```
SUP basecalling
```
ulana -q 10 -l 1500 -c 56 -i sup_basecalled_reads.fastq -b r941_min_sup_g507
```

# Workflow illustration

![](ulana_pipeline.jpg)
