# python-shortcuts
simple tricks and tips for efficient coding in python 

## Channel changing in images

cv2 reads RGB format most of thae packages runs on BGR so convert RGB to BGR

    rgb_frame = frame[:, :, ::-1]
    
 ## Reads a  floder files from directory
````

for dirname, _, filenames in os.walk('/content/gdrive/My Drive/New/'):
    for filename in filenames:
        cap = cv2.VideoCapture(dirname+'/'+filename)
        
        if not os.path.exists(filename):
            os.mkdir(filename)
```` 
