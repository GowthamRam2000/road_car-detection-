## Running the code

`roads_cars.py` uses transfer learning from VGG16 to train whether to identify roads or cars. `roads_cars.py` is run using the following arguments:

`'type'`: choices=['roads','cars'], help="Choose the type of model to train/load - either a model for cars or roads"
`'-v'`, help="When passing v, a model will be loaded and validated using validation images. If this argument is not passed, then a new model will be trained and stored in the models folder."
`'-p'`, help="Persist image."
`'-s'`, help="Show image in a pop-up window."

`no_pretrain_roads_cars.py` uses an FCN architecure to train whether to identify only roads and trains it from scratch. This does not train a model to identify cars since the other approach works much better. `no_pretrain_roads_cars.py` is run using the following arguments:

`'architecture'`, choices=['1','2'], help="Choose the architecture to use 1 is nearest neighbour upsampling and 2 is transposed convolution for the upsamplling procedure"
`'-v'`, help="When passing v, a model will be loaded and validated using validation images. If this argument is not passed, then a new model will be trained and stored in the models folder."
`'-p'`, help="Persist image."
`'-s'`, help="Show image."

predict_traffic.py takes the pixels where they are predicted roads and the pixels where they are predicted cars and determines what percentage of the road is filled with cars to get the level of traffic.
