# PolyGoneNMS

PolyGoneNMS is a library for efficient and distributed polygon Non-Maximum Suppression (NMS) in Python. It supports various NMS methods, intersection calculations, and can handle large numbers of polygons in 1D, 2D, and 3D spaces. PolyGoneNMS uses R-tree data structures and shapely polygon objects for optimal performance.

## Features
- Efficient polygon NMS for large numbers of polygons.
- Support for various NMS methods: Default, Soft, and Class Agnostic.
- Support for different intersection methods: IOU, IOS, and Dice.
- R-tree data structure for efficient spatial indexing and querying.
- Distributed processing support using Ray and Dask.
- Comprehensive documentation and examples.

## Installation

You can install PolyGoneNMS using pip:

```bash
pip install polygone-nms
```

## Quickstart

```python
import numpy as np
from polygone_nms import polygone_nms

# Example input data
data = np.array([
    [0, 0, 1, 1, 0, 1, 0, 0, 1, 0.9],
    [0.5, 0.5, 1.5, 1.5, 0.5, 1.5, 0, 0, 1, 0.8],
])

# Apply NMS
results = polygone_nms(data, distributed=None, nms_method="Default", intersection_method="IOU")

print(results)
```

For a more detailed guide on using PolyGoneNMS, please see the [Quickstart](https://www.example.com/) in the documentation.

## Documentation

Detailed documentation is available at TODO.

## Contributing

We welcome contributions to the project! Please follow the usual GitHub process for submitting issues or pull requests.

## License

This project is licensed under the [MIT License](https://fossa.com/blog/open-source-licenses-101-mit-license/).
