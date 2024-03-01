# Environment Configuration

```bash
conda create -n kits python=3.8
conda activate kits
pip3 install torch==1.8.2 torchvision==0.9.2 torchaudio==0.8.2 --extra-index-url https://download.pytorch.org/whl/lts/1.8/cu111
pip install torchmetrics==0.4.0
pip install pytorch-lightning==1.4.0
pip install tables==3.7.0
```

Then manually change `np.bool` to `np.bool_`.

Download the datasets.zip  [here](https://drive.google.com/file/d/1aFy30dpsq3GSTBO5fUeO3PdaaueJHjJL/view?usp=sharing), and unzip it to the current path.

Training:

```
python train.py --config config/kits/la_point.yaml --miss-rate 0.5 --lr 0.0002 --patience 50
```

