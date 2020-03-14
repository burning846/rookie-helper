# Image Process 图像处理

### numpy

- 新建一张RGB纯色图片

```python
import numpy as np
np.full((h, w, 3), [255, 0, 0]).astype(np.uint8)
```

- 新建一张和原图一样大的mask

```python
import numpy as np
np.zeros(img.shape[:2])
```

### OpenCV

- 绘制多边形

```python
import cv2
import numpy as np
output = np.zeros((100, 100, 3)).astype(np.uint8)
poly = np.array([[1,2],[1,30], [30,30], [30,1]])
output = cv2.fillPoly(output, [poly], (255, 0, 0))
```