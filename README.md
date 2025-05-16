# Depth-Estimation

In this work, we investigate the impact of three attention mechanisms — Channel Attention (CA),
Spatial Attention (SA), and Convolutional Block Attention Module (CBAM) — when integrated
into popular CNN architectures. The models explored include ResNet-50, ResNet-100, and
DenseNet-121. These models were trained and evaluated on the DIODE dataset, which provides
dense depth maps for a wide range of indoor and outdoor scenes. Additionally, experiments were also
conducted on the NYU Depth V2 dataset using the DenseNet-121 backbone, which focuses on
indoor environments.

Designed an architecture with 3 main components.
1) Encoder - ResNet-50, ResNet101, DenseNet-121
2) Decoder - 5 Layers
3) Attention Mechanism - CA, SA, CBAM

Attention Mechanism Overview:
1) Channel Attention (CA): Emphasizes important feature channels by applying global average and
max pooling followed by MLP layers.
2) Spatial Attention (SA): Highlights important spatial locations in the feature map using 2D
pooling and convolution.
3) CBAM (Convolutional Block Attention Module): Combines both CA and SA sequentially for a
more comprehensive focus mechanism.

The following configurations were implemented:
1) ResNet-50 + CA / SA / CBAM (on DIODE)
2) ResNet-101 + CA / SA / CBAM (on DIODE)
3) DenseNet-121 + CA / SA / CBAM (on DIODE and NYU)

Standard depth estimation metrics were used:
1) Root Mean Square Error (RMSE)
2) Mean Absolute Error (MAE)
3) Relative Error (REL)

All jupyter Notebooks and models trained are available above.