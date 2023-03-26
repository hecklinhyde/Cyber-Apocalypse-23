# Description
Thousands of years ago, sending a GET request to /flag would grant immense power and wisdom. Now it's broken and usually returns random data, but keep trying, and you might get lucky... Legends say it works once every 1000 tries.

# Thoughts 
Python time! 

```
import socket
import re
import requests as req

for i in range(1001):
	resp=req.get("http://{IP}/flag")
	print(resp.text)
	print(i)
	if 1==1000:
print(resp.text)
```

# Solve
300 requests later
## HTB{y0u_h4v3_p0w3rfuL_sCr1pt1ng_ab1lit13S!}
