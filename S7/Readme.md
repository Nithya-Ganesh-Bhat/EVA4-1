This model implemented the first use of CIFAR. Here we have used all the concepts as mentioned in Session 7.

1)	Dropout
2)	Batch Normalization
3)	Depthwise Seperable Convolution
4)	Dilated convolution
5)	Utility Function
6)	Training and testing function 
7)	Accuracy Functions

Top Accuracy = 82.31% (14th Epoch) 
We have reached Receptive Field of 60 which is shown in the Model.py file as comments.


Receptive Field Calculation

| K,p,s         	| Image 	| RF (in) 	| RF (out) 	| J(out) 	|
|---------------	|-------	|---------	|----------	|--------	|
| 3,1,1         	| 32    	| 1       	| 3        	| 1      	|
| 3,1,1         	| 32    	| 3       	| 5        	| 1      	|
| 2,0,2 (MP)    	| 16    	| 5       	| 6        	| 1      	|
| 3,1,1         	| 16    	| 6       	| 10       	| 2      	|
| 3,1,1         	| 16    	| 10      	| 14       	| 2      	|
| 2,0,2 (MP)    	| 8     	| 14      	| 16       	| 2      	|
| 3,1,1         	| 8     	| 16      	| 24       	| 4      	|
| 5,2,1 (Dil=2) 	| 8     	| 24      	| 40       	| 4      	|
| 2,0,2 (MP)    	| 4     	| 40      	| 44       	| 4      	|
| 3,1,1         	| 4     	| 44      	| 60       	| 8      	|
