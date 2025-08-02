FROM runpod/pytorch:2.8.0-py3.11-cuda12.8.1-cudnn-devel-ubuntu22.04

RUN apt update && apt install -y git curl wget python3-pip ffmpeg

WORKDIR /workspace
RUN git clone https://github.com/comfyanonymous/ComfyUI.git .
RUN pip install -r requirements.txt

CMD ["python3", "main.py", "--listen", "0.0.0.0", "--port", "8188"]
