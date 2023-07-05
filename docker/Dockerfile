FROM pytorch/pytorch:1.11.0-cuda11.3-cudnn8-devel

# needed to allow apt update
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A4B469963BF863CC

RUN apt update && apt install -y \
    libturbojpeg \
    ffmpeg \
    libsm6 \
    libxrender1 \
    libfontconfig1 \
    freeglut3-dev \
    llvm-6.0 \
    llvm-6.0-tools \
    git \
    wget \
    vim

COPY requirements.txt /opt/app/requirements.txt

WORKDIR /opt/app

RUN pip install -r requirements.txt

RUN mkdir -p /PARE

WORKDIR /PARE
