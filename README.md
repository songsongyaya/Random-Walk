# Random-Walk
import numpy as np
np.random.seed(123)
random_walk=[0]
for x in range(100):
    step=random_walk[-1]
    dice=np.random.randint(1,7)
    #determine next step
    if dice<=2:
        #use max to make sure step cannot go below 0
        step=max(0,step-1)
    elif dice>=3 and dice<=5:
        step=step+1
    else:
        step=step+np.random.randint(1,7)
    #append step to random_walk
    random_walk.append(step) 
print(rando_Walk)
#visualize the walk
import matplotlib.pyplot as plt
plt.plot(random_walk)
plt.show()
 
