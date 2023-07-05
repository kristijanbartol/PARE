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
    wget 

COPY requirements.txt /opt/app/requirements.txt

WORKDIR /opt/app

RUN pip install -r requirements.txt

#RUN python3.8 -m pip install \
#	numpy==1.23.1 \
#	torch==1.11.0 \
#	torchvision==0.12.0 \
#	joblib==0.15.1 \
#	opencv-python==4.1.1.26 \
#	trimesh>=4.1.1.26 \
#	pyrender>=0.1.36 \
#	smplx>=0.1.28 \
#	tqdm>=4.47.0 \
#	loguru>=0.3.2 \
#	albumentations>=0.4.6 \
#	scipy>=1.7.0 \
#	pyyaml>=5.3.1 \
#	yacs>=0.1.8 \
#	matplotlib>=3.4.2 \
#	scikit-image>=0.17.2 \
#	pillow>=8.2.0 \
#	pytorch-lightning>=1.1.8 \
#	numba>=0.54.1 \
#	filterpy>=1.4.5 \
#	flatten-dict>=0.2.0 \
#	fastai>=1.0.55 \
#	jpeg4py>=0.1.4 \
#	chumpy>=0.70 \
#	torchgeometry>=0.1.2 \
#	setuptools>=47.3.1 \
#	git+https://github.com/mkocabas/yolov3-pytorch.git \
#	git+https://github.com/mkocabas/multi-person-tracker.git \
#	git+https://github.com/giacaglia/pytube.git

RUN mkdir -p /PARE

WORKDIR /PARE
