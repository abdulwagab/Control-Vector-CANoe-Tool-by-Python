# Control-Vector-CANoe-Tool-by-Python
pip install Python-CANoe
----------------------------------------------------------------------------------------
README.md (File)

Control Vector CANoe API by Python

Install:

pip install Python-CANoe

Usage:

app = CANoe.CANoe() #Define CANoe as app

app.open_simulation("test.cfg") #import a CANoe congif

app.start_Measurement() #Start CANoe

var_from_namespace = app.get_all_SysVar("mfl") #Get all system variables under namespace

print(app.get_SysVar("mfl","vol_plus")) #Get the value of the system variable

app.set_SysVar("mfl","vol_plus",1) #Write the value of the system variable

app.stop_Measurement() #stop CANoe


--------------------------------------------------------------------------------------------------------
Sample.py (File)

# -*- coding: UTF-8 -*-
#.Data:2018/5/19

import CANoe
import time

app = CANoe.CANoe() #Define CANoe as app

app.open_simulation("test.cfg") #import a CANoe congif

app.start_Measurement() #Start CANoe

var_from_namespace = app.get_all_SysVar("mfl") #Get all system variables under namespace

print(app.get_SysVar("mfl","vol_plus")) #Get the value of the system variable

app.set_SysVar("mfl","vol_plus",1) #Write the value of the system variable

app.stop_Measurement() #stop CANoe

----------------------------------------------------------------------------------------------------
setup.py (File)

# -*- coding: UTF-8 -*-
#.Data:2018/5/19
from setuptools import setup

setup(name='Python_Vector_CANoe',
      version='0.1',
      description='Control Vector CANoe API by Python',
      url='https://github.com/hmq2018/Python-Vector-CANoe',
      author='Hz',
      author_email='weld83@126.com',
      license='MIT',
      packages=['Python_Vector_CANoe'],
      install_requires=[
          'pywin32==301',
      ],
      zip_safe=False)

-------------------------------------------------------------------------------------------------
CANoe/__init__.py (File)

# -*- coding: UTF-8 -*-
#.Data:2018/5/19

from .Python_CANoe import CANoe  # hz

------------------------------------------------------
