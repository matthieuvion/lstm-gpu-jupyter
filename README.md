## Benchmark - time series prediction LSTM PyTorch
 


- Noteboook *updated from this source [article](https://machinelearningmastery.com/lstm-for-time-series-prediction-in-pytorch/)*, with a famous dataset  
- *What was **added** :*  
    - clarifies steps / order making data stationary / normalization (a common mistake/lack of in a lot of online ressources)
    - Make data stationary (first order diff). Not mandatory with a lstm but very common, recommended and usually improves performance
    - More structure / pipelined : transform functions (normalize / inverse diff via cumsum etc.), steps / notes on arrays shape etc.   
    - Normalization (minmax)
    - Input size (lookback) directly set to 4 (vs. 1, then 4)
    - benchmark/viz models accuracy with and without statio. + scaling

> Run:    
> Personally, running it in a dockerized, gpu/cuda-enabled pytorch/notebook environment (cf. [github/gpu-jupyter](https://github.com/iot-salzburg/gpu-jupyter))  