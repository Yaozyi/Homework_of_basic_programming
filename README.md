# Homework_of_basic_programming

本次进行分析探讨的数据集来自Kaggle上Acea举办的一次关于水体预测的比赛项目(https://www.kaggle.com/competitions/acea-water-prediction/data)，项目需要参赛者通过对易于得到的降雨量，温度等变量对水位的预测，便于水务部门处理日常用水问题。

该数据集中含有水库、泉水、河流、湖泊四类水体的有关的对应城市数据，而本篇报告则关注地下水的水位问题，数据集是Petrignano有关地下水的信息，包括八个变量，分别是：

\textbf{时间}:(date)表示检测该条数据监测的时间，精确到以天为单位。

\textbf{降雨量}:(Rainfall\_Bastia\_Umbra)表示意大利城市巴斯蒂亚温布拉的降雨量，单位为毫米（mm）.

\textbf{水位}:(Depth\_to\_Groundwater\_P24)(Depth\_to\_Groundwater\_P25):它表示由测压计P24,P25检测到的地下水位，以距离地面的高度表示，单位为米(m)。

\textbf{温度}(Temperature\_Bastia\_Umbra):表示巴斯蒂亚温布拉测温站检测到的温度，单位为°C.

\textbf{温度}:(Temperature\_Petrignano):表示在彼得里尼亚诺处检测到的温度，单位为°C.

\textbf{排水量}:(Volume\_C10):表示提取的饮用水的体积，单位为立方米($m^3$).

\textbf{河水深度}:(Hydrometry\_H):表示水文站检测到的地下水位，单位为米（m）.

在本篇分析报告中，建立了五种模型对地下水深度进行预测，并用MAE与RMSE为度量进行模型的比较。

进行复现时，所配置的环境如下：

Package                 Version
----------------------- ------------
absl-py                 1.4.0
aiohttp                 3.9.0
aiosignal               1.2.0
arviz                   0.16.0
asttokens               2.4.1
astunparse              1.6.3
async-timeout           4.0.2
attrs                   23.1.0
blinker                 1.6.2
Bottleneck              1.3.5
Brotli                  1.0.9
cachetools              4.2.2
certifi                 2023.11.17
cffi                    1.16.0
charset-normalizer      2.0.4
click                   8.1.7
cmdstanpy               1.1.0
colorama                0.4.6
comm                    0.1.4
contourpy               1.2.0
convertdate             2.3.2
cryptography            41.0.3
cycler                  0.11.0
Cython                  3.0.0
debugpy                 1.8.0
decorator               5.1.1
ephem                   4.1.2
exceptiongroup          1.2.0
executing               2.0.1
flatbuffers             2.0
fonttools               4.25.0
frozenlist              1.4.0
gast                    0.4.0
google-auth             2.22.0
google-auth-oauthlib    0.4.4
google-pasta            0.2.0
grpcio                  1.48.2
h5netcdf                1.2.0
h5py                    3.9.0
holidays                0.29
idna                    3.4
importlib-metadata      6.0.0
importlib-resources     6.1.0
ipykernel               6.26.0
ipython                 8.18.1
jedi                    0.19.1
Jinja2                  3.1.2
joblib                  1.2.0
jupyter_client          8.6.0
jupyter_core            5.5.0
keras                   2.10.0
Keras-Preprocessing     1.1.2
kiwisolver              1.4.4
LunarCalendar           0.0.9
Markdown                3.4.1
MarkupSafe              2.1.1
matplotlib              3.8.0
matplotlib-inline       0.1.6
mkl-fft                 1.3.8
mkl-random              1.2.4
mkl-service             2.4.0
multidict               6.0.4
munkres                 1.1.4
nest-asyncio            1.5.8
numexpr                 2.8.7
numpy                   1.26.2
oauthlib                3.2.2
opt-einsum              3.3.0
packaging               23.1
pandas                  2.1.4
parso                   0.8.3
patsy                   0.5.3
pickleshare             0.7.5
Pillow                  10.0.1
pip                     23.3.1
platformdirs            4.1.0
pmdarima                2.0.3
prompt-toolkit          3.0.42
prophet                 1.1.4
protobuf                3.20.3
psutil                  5.9.5
pure-eval               0.2.2
pyasn1                  0.4.8
pyasn1-modules          0.2.8
pycparser               2.21
Pygments                2.17.2
PyJWT                   2.4.0
PyMeeus                 0.5.11
pyOpenSSL               23.2.0
pyparsing               3.0.9
PySocks                 1.7.1
pystan                  2.19.1.1
python-dateutil         2.8.2
pytz                    2023.3.post1
pywin32                 306
pyzmq                   25.1.2
requests                2.31.0
requests-oauthlib       1.3.0
rsa                     4.7.2
scikit-learn            1.3.0
scipy                   1.11.4
seaborn                 0.12.2
setuptools              68.2.2
six                     1.16.0
stack-data              0.6.2
statsmodels             0.14.0
tensorboard             2.10.0
tensorboard-data-server 0.6.1
tensorboard-plugin-wit  1.8.1
tensorflow              2.10.0
tensorflow-estimator    2.10.0
termcolor               2.1.0
threadpoolctl           2.2.0
tornado                 6.3.3
tqdm                    4.65.0
traitlets               5.14.0
typing_extensions       4.7.1
tzdata                  2023.3
urllib3                 1.26.18
wcwidth                 0.2.12
Werkzeug                2.2.3
wheel                   0.41.2
win-inet-pton           1.1.0
wrapt                   1.14.1
xarray                  2023.6.0
xarray-einstats         0.6.0
yarl                    1.9.3
zipp                    3.11.0
