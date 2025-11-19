# Morph-Tool

Morph-Tool is a rule-based **Kannada Morphological Analyzer** forming the final stage of a 3-step NLP pipeline:

1. POS Tagging  
2. Chunking  
3. Morphological Analysis  

---

## 📁 Repository Structure

```
Morph-Tool/
│
├── morphtool.sh                  # Main script to run morphological analysis
├── category_map.py               # POS → Morph category mapping rules
├── charsreplace.py               # Character normalization rules
├── gender_number.py              # Gender and number predictor module
├── morph_hash.py                 # Hash-based morphological lookup
├── replaceback.py                # Restores original chars after processing
├── rootadd.py                    # Adds root forms using rule-based logic
├── suff_dict.py                  # Suffix dictionary
├── suffix_morpheme_dict.py       # Morph + suffix identification rules
├── template_root_dict.py         # Template-based root extraction
├── template_suffix_dict.py       # Template-based suffix extraction
│
├── exceptional_words.txt         # List of irregular / exceptional words
├── exceptions.txt                # Additional exception rules
├── rootsandsuff.txt              # Root + suffix mapping pairs
│
├── all_available_data.pickle     # Combined morphology resource file
└── Splitter/                     # Module for splitting morphological units
```

---

## 🛠 Requirements

- Python 3.x  
- Perl  
- Linux/macOS recommended  

---

## ▶ Usage

Run the Morph Tool:

```bash
sh morphtool.sh inputfile outputfile
```

### Example:

```bash
sh morphtool.sh chunk_output.conll morph_output.conll
```

---

## 📌 Full Pipeline

```bash
python run_pos_new.py --input inputfile --output pos_output --model xlm-base-2
sh run_chunk.sh pos_output chunk_output checkpoint-18381
sh morphtool.sh chunk_output morph_output
```

---
