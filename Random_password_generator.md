```python
from random import sample,shuffle
character_list=['abcdefghijklmnopqrstuvwxyz','ABCDEFGHIJKLMNOPQRSTUVWXYZ','0123456789','@#$%^&*']
```
```python
password=[]
least_type=sample((3,4),1)[0]
for i in sample([0,1,2,3],least_type):
    password.append(sample(character_list[i],1)[0])
spare=sample(range(10-least_type,21-least_type),1)[0]
for i in range(spare):
    password.append(sample(''.join(character_list),1)[0])
shuffle(password)
print(''.join(password))
```
