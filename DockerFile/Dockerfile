FROM pytorch/pytorch

RUN apt update
RUN apt install -y git

RUN conda install -c conda-forge --name base --update-deps --force-reinstall ipykernel

RUN pip3 install pandas matplotlib albumentations segmentation_models_pytorch eo-learn nbconvert MarkupSafe==2.0.1 torchgeo ipywidgets radiant_mlhub tabulate torchinfo image_slicer


RUN pip install -U torch-tb-profiler
RUN apt-get update

RUN echo "/usr/local/lib/python3.7/site-packages/" > /opt/conda/lib/python3.7/site-packages/usrlocal.pth
RUN cd /usr/local/lib && ldconfig

RUN pip install -U imbalanced-learn
RUN pip install seaborn