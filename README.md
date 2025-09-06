### 1. Determining Sankey's color by the proportion of TypeA[^1]
[^1]: Lai, Y., & Zhao, H. (2025). Comparative analysis of smart city scientific research trends in the USA and China. Nature Cities, 1～9. https://doi.org/10.1038/s44284-025-00305-y  
- **Applicable to situations where flow types are distinguished (TypeA and TypeB)**
#### 1.1 Necessary packages
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import pickle
from collections import defaultdict
import matplotlib.colors as mcolors
import plotly.graph_objects as go
```
#### 1.2 Data description
- **source:** Source of flow  
- **target:** Target of flow  
- **typeA:** Flow quantity of TypeA  
- **typeB:** Flow quantity of TypeB  
- **total:** Total flow quantity of TypeA and TypeB  

<img width="1220" height="351" alt="image" src="https://github.com/user-attachments/assets/ad282de4-ac4b-4a7a-bcfe-bfac7bbd38ce" />
<div align="center">
  <b>Fig.1</b> Data description
</div>

#### 1.3 Result display
- **inactive**
<img width="1764" height="1695" alt="image" src="https://github.com/user-attachments/assets/38a05d39-94ff-47d5-b822-6585b6e3033b" />
<div align="center">
  <b>Fig.2</b> Inactive display
</div>

- **interactive**: Try to manipulate the chart through **"Box select"**
<img width="1737" height="1721" alt="image" src="https://github.com/user-attachments/assets/398b2dd1-cfbd-4fc9-8f5b-3dccb291fe49" />
<div align="center">
  <b>Fig.3</b> Interactive display
</div>

### 2. Determining Sankey's color at random
- **Applicable to situations where flow types are not distinguished (only the total number of flow)**
- **Set random seed**
```python
import random
random.seed(42)
link_colors = [grad_color(random.random()) for _ in range(len(df))]
```
- **Result**
<img width="1682" height="1707" alt="image" src="https://github.com/user-attachments/assets/8ebbe004-b652-47b5-9e93-0e0ee027bff1" />
<div align="center">
<b>Fig.4</b> Radom color
</div>
