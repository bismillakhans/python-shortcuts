# python-shortcuts:smile:
simple tricks and tips for efficient coding in python 

## Channel changing in images

cv2 reads RGB format most of thae packages runs on BGR so convert RGB to BGR

    rgb_frame = frame[:, :, ::-1]
    
 ## Reads a  FOLDER files from directory:bug:
````

for dirname, _, filenames in os.walk('/content/gdrive/My Drive/New/'):
    for filename in filenames:
        cap = cv2.VideoCapture(dirname+'/'+filename)
        
        if not os.path.exists(filename):
            os.mkdir(filename)
```` 
## convert image in to octect stream :hand:

````
    frame=cv2.imread('image.png')
    ret,buf = cv2.imencode('.png', frame)
    # ret,buf2 = cv2.imencode('.png', frame)

    # stream-ify the buffer
    stream = io.BytesIO(buf)
````
## list conversion:train:
````
list(map(lambda x: x.face_id, faces_1))

````

## writing condition in list:train:

````
 next(x for x in faces_1 if x.face_id == face_ID)
````

### advanced python array unpacking :handbag:
````
regions = ['pfc', 'ifg', 'sts', 'atl', 'acc']
first, *rest, last = regions
````
### array filtering using lamda function :spider_web:

````
data = [(3, 4), (1, 2), (0, 1), (2, 7), (3, 3)]
list(filter(lambda x: sum(x) > 5, data))
````
## sample .env files for django

````
SECRET_KEY=sample
DEBUG=False
ALLOWED_HOSTS=127.0.0.1
SQL_ENGINE=django.db.backends.postgresql_psycopg2
SQL_DATABASE=
SQL_USER=
SQL_PASSWORD=
SQL_HOST=
SQL_PORT=
USE_S3=true
AWS_STORAGE_BUCKET_NAME=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY_ID=
````


##Generate random secret key in Python :random:

````
from binascii import hexlify
key = hexlify(os.urandom(20))
key.decode()
````

