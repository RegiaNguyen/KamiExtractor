# KamiExtractor 🌿

A **Windows-friendly Wikipedia Extractor**.  
Convert Wikipedia dump files (`.xml.bz2`) into clean and ready-to-use **JSONL** format for ML/AI pretraining.

✨ Why KamiExtractor?
- Original [WikiExtractor](https://github.com/attardi/wikiextractor) is great, but heavily biased towards Linux/Unix environments.
- Running on Windows often causes issues (`fork`, `bzcat`, path errors, etc.).
- KamiExtractor is a lightweight, Python-only extractor that **just works on Windows**.
- Born after 8+ hours of fighting Linux-biased code at 2AM.  
- It just works™.

---

## Features
- ✅ Parse `.xml.bz2` Wikipedia dumps
- ✅ Output JSONL files (`.jsonl`)
- ✅ Configurable limit on number of pages
- ✅ Handles namespaces filtering
- ✅ Designed for **Windows compatibility**

---

## Quick Start

git clone https://github.com/YOUR_USERNAME/KamiExtractor.git
cd KamiExtractor

# Run extractor (💡 On Windows PowerShell, replace \ with ` for line continuation.)

python tools/mini_extractor.py \
  --input path/to/viwiki-latest-pages-articles.xml.bz2 \
  --output extracted_viwiki \
  --json \
  --max-bytes 104857600 \
  --limit 100000
