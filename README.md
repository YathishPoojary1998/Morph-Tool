# Morph-Tool

Morph-Tool is a rule-based **Kannada Morphological Analyzer**.  
It forms the **final stage** in a 3-step NLP pipeline:

1. POS Tagging  
2. Chunking  
3. Morphological Analysis  

## Repository Structure
(See project folders)

## Requirements
- Python 3.x
- Perl
- Linux/macOS recommended

## Usage
```bash
sh morphtool.sh inputfile outputfile
```

## Pipeline
```bash
python run_pos_new.py --input inputfile --output pos_output --model xlm-base-2
sh run_chunk.sh pos_output chunk_output checkpoint-18381
sh morphtool.sh chunk_output morph_output
```

## License
Add your license here.
