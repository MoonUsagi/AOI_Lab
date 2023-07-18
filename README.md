# AOI Lab(影像辨識與檢測)
Bulit on 2023/07 by Fred Liu  

版本:MATALB: 2023a ~ 最新版本  
需要工具箱: Deeplearning , Image Processing, Computer Vision, Parallel Computing  
需要支援包: 
Computer Vision Toolbox Model for Text Detection,  
Computer Vision Toolbox OCR Language Data,  
Computer Vision Toolbox Automated Visual Inspection Library  
  
  
## 1.TextDetection  
針對影像中的文字檢測並且標記，利用detectTextCRAFT模型。
> AOI_TextDetection.mlx  
  
![image](https://github.com/MoonUsagi/AOI_Lab/blob/main/image/r01.JPG)  


## 2.OCR  
針對文字做辨識，在2023a後的版本中，OCR的裡面的模型改為是Tesseract 5.0，演算法核心Deep Learning base，
架構為CNN+LSTM，所以整體精準度都有提高，目前也有62種語言與數字顯示器的辨識模型，並且可以在
> AOI_DeepOCR.mlx  
> AOI_TrainDeepOCR.mlx  
> AOI_QuantizeOCR.mlx  
  
![image](https://github.com/MoonUsagi/AOI_Lab/blob/main/image/r02.JPG)  

## 3.BarCodeRead
針對一維與二維條碼，進行檢測與辨識。
> AOI_BardcodeRead.mlx  
  
![image](https://github.com/MoonUsagi/AOI_Lab/blob/main/image/r05.jpg)  



## 4.Anomaly Detection  
影像異常偵測與缺陷辨識，2022b之後的版本更新了三種異常偵測的演算法，分別是:  
<style>
table th:first-of-type {
    width: 20%;
}
table th:nth-of-type(2) {
    width: 30%;
}
table th:nth-of-type(3) {
    width: 50%;
}
</style>

  
| Network | Function |Notes|
|---|:---:|-------|
|FCDD|fcddAnomalyDetector<br>trainFCDDAnomalyDetector|．Light-weight model<br>．Fully convolutional<br>．Supports tiled training / full size inference workflow<br>|
|FastFlow|fastFlowAnomalyDetector<br>trainFastFlowAnomalyDetector|．State-of-the-Art model<br>．Fully convolutional<br>．Supports tiled training / full size inference workflow<br>．Relatively Memory intensive|
|PatchCore|patchCoreAnomalyDetector<br>trainPatchCoreAnomalyDetector|．State-of-the-Art model<br>．Feature similarity based(no gradient descent training involved)<br>．Few-shot training<br>．Fixed image size at train and test<br>．Relatively Memory intensive(Supports compression)|


> AOI_AnomalyDetection.mlx　　

![image](https://github.com/MoonUsagi/AOI_Lab/blob/main/image/ad01.PNG)  
![image](https://github.com/MoonUsagi/AOI_Lab/blob/main/image/ad02.PNG)
  