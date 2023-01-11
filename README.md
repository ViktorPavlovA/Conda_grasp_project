# Курсовая работа по машинному обучению

**Выполнили Павлов В. Горин Н. Матвеев К. Сизов Е.**

Использована OS: Windows 10 home

## Первое, что нужно сделать это установить anaconda

[Здесь](https://www.anaconda.com/products/distribution)

## После установки

1. Перейти в приложение  Anaconda Prompt (Anaconda3)

`dir` - посмотреть содержимое директории

`cd _папка_` - переход в **_папку_**

`mkdir grasping_conda` - создать папку **grasping_conda**

Простой пример:

`(base) C:\Users\Viktor>cd Desktop`

Я установил среду в папке на рабочем столе:

`(base) C:\Users\Viktor\Desktop>mkdir grasping_conda`

`cd grasping_conda`

2. В папке установим среду

`conda create -n grasp_env python=3.6`

`conda activate grasp_env`

3. Перед установкой следующего пакета необходимо перейти в папку где у вас храниться anaconda 

`anaconda anaconda3>Library>bin`

**Найдите эти два файла:**

`libcrypto-1_1-x64.dll`

`libssl-1_1-x64.dll`

**и скопируйте в anaconda3>DLLs**

4. Установим дополнительные пакеты

`conda install git`

`git clone https://github.com/BarisYazici/deep-rl-grasping.git`

`conda install -c conda-forge cudatoolkit=10.0 cudnn=7.6.5`

`SET LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/`

5. Изменим setup.py

Для этого выполним предполагается, что у вас установлен vscode

[VSCODE](https://code.visualstudio.com/download)

В принципе подойдет любой текстовый редактор

`code .`

`'tensorflow==1.14.0'`

На

`'tensorflow_gpu==1.14.0'`

## Финальная установка

`pip install -e .`

