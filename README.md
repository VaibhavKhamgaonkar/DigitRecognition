# DigitRecognition
Digit identification using Python and Neural Network
Train and test data files are added for training the model.
It consist of 0 to 9 digit (28,28) pixel numeric data.


## To do the prediction :
#loading the saved model
m = load_model('/Users/Digit.h5') # path of stored model

#definging the functiuon to perform prediction

def predictDigit(imgNum):
    img = cv2.imread('/Users/' + str(imgNum), 0) # location of image 
    print(img.shape)
    #img = cv2.resize(img, (28,28))
    img = img.reshape(1,28,28,1)
    predict = m.predict_classes(img)
    print(dM.predict(img))
    print ('Digit is {}'.format(predict))
    
    
    
predictDigit('img1.jpg')



Output is 
(28, 28)
[[1. 0. 0. 0. 0. 0. 0. 0. 0. 0.]]
Digit is [0]
