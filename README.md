# ComfyUIMacIntel
Installing ComfyUI on a MacIntel

This is something I thought would be useful if you have a Macbook with an Intel processor as for now info I've found is only available for the Apple Silicon platform
I took inspiration from
https://www.youtube.com/watch?v=oyNrJRyTdG8
and
https://stable-diffusion-art.com/how-to-install-comfyui/#Installing_ComfyUI_on_Mac_M1M2

First thing first, my MBP didn't have Homebrew, so in a shell type
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Takes a bit to get it installed, couple extra packages are required
brew install cmake protobuf rust python@3.10 git wget

Clone ComfyUI
git clone https://github.com/comfyanonymous/ComfyUI

Get there
cd ComfyUI

Create Virtual Env
python -m venv venv

Install PyTorch in that Virtual Env
./venv/bin/pip install torch torchvision torchaudio

Install the required packages for Comfy
./venv/bin/pip install -r requirements.txt

Something that may sound dumb, but you have created a ComfyUI in your user folder, this is where you find the folder structure to set the files you download:
SDXL Models Download Links
https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0/blob/main/sd_xl_base_1.0.safetensors
https://huggingface.co/stabilityai/stable-diffusion-xl-refiner-1.0/blob/main/sd_xl_refiner_1.0.safetensors

SDXL VAE
https://huggingface.co/stabilityai/sdxl-vae/blob/main/sdxl_vae.safetensors

I create a Stable-diffusion folder to match the syntax in the video and put the safetensors there. There's already a VAE folder so I ust add the SDWL VAE file there

Maybe useful to manage the ComfyUI environment
https://github.com/ltdrdata/ComfyUI-Manager



Enjoy ComfyUI!
Some good tips here https://github.com/cubiq/ComfyUI_Workflows/blob/main/basic/README.md



