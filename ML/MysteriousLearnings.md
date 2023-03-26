# Description
One day the archeologist came across a strange metal plate covered in uncommon hieroglyphics. It looked like blueprints for some kind of alien technology. "What kind of magic is this?" He studied the plate more closely and was amazed by the advanced technology and incredible engineering they were using at a time like this. This could only lead him in him wanting to learn more...

# Thoughts 
Tensorflow, keras recieved an .h5 file.

```
import tensorflow as tf
from tensorflow import keras
alienModel = tf.keras.models.load_model('/content/sample_data/alien.h5')
print(alienModel.summary())
```
![Mysterious Learnings model](/screencaps/ML_learnings.jpg)

# Solve
Put the weird responses together and base 64 decode! 

```
import base64
alienString="SFRCe24wdF9zb19oNHJkX3RvX3VuZDNyc3Q0bmR9="
humanString=base64.b64decode(alienString)
print(humanString)
```
