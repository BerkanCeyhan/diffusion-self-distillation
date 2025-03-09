# Run Instructions for Windows

- Python 3.12 runterladen

Dann folgendes dependencies installieren.
```
pip install -r requirements.txt
```

## Folgende Dateien laden 
Download Link: [Google Drive](https://drive.google.com/drive/folders/1VStt7J2whm5RRloa4NK1hGTHuS9WiTfO?usp=sharing)

## Ordnerstruktur erstellen
- `transformers`
    - `config.json`
    - `diffusion_pytorch_model.safetensors`
- `pytorch_lora_weights.safetensors`


<!-- 
### 🔧 Configuration
--> 

## Parameter anpassen und ausführen:

Parameter: 
- guidance 3.5 
- i_guidance 1.0 
- t_guidance 1.0


```bash
$env:CUDA_VISIBLE_DEVICES = "0"
py -3.12 -m generate --model_path transformer --lora_path pytorch_lora_weights.safetensors --image_path INPUT_PATH --text "PROMPT einfügen" --output_path OUTPUT_PATH --guidance 3.5 --i_guidance 1.0 --t_guidance 1.0
```


Beispiel:
```bash
$env:CUDA_VISIBLE_DEVICES = "0"
py -3.12 -m generate --model_path transformer --lora_path pytorch_lora_weights.safetensors --image_path images\example.png --text "this characters playing soccer in the snow" --output_path output\output.png --guidance 3.5 --i_guidance 1.0 --t_guidance 1.0
```