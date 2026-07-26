# Tensors

A **tensor** is a data structure (container) used to store numerical data. It is the fundamental data representation used in deep learning libraries such as **TensorFlow** and **PyTorch**. *(Scikit-learn primarily uses NumPy arrays, which are tensor-like.)*

> **Key Rule:**
> **Number of Axes = Number of Dimensions = Rank**

---

## 0D Tensor (Scalar)

A single numerical value.

```text
5
```

* **Rank:** 0
* **Shape:** `()`

---

## 1D Tensor (Vector)

A collection of scalars.

```text
[1, 2, 3]
```

* **Rank:** 1
* **Shape:** `(3,)`

> A **vector** is simply a 1D tensor.

---

## 2D Tensor (Matrix)

A collection of vectors.

### Example 1

```text
[
 [1, 2, 3],
 [4, 5, 6]
]
```

* **Shape:** `(2, 3)`

### Example 2

```text
[
 [1, 2, 3],
 [4, 5, 6],
 [7, 8, 9]
]
```

* **Shape:** `(3, 3)`

> A **matrix** is a 2D tensor.

---

## 3D Tensor

A collection of matrices.

```text
[
  [
    [1,0,0,0],
    [0,1,0,0]
  ],
  [
    [1,0,0,0],
    [0,0,1,0]
  ],
  [
    [1,0,0,0],
    [0,0,0,1]
  ]
]
```

* **Shape:** `(3, 2, 4)`

### Real-World Example

Suppose you record the **highest** and **lowest** temperatures for **365 days** over **10 years**.

```text
Shape = (10, 365, 2)
```

where:

* `10` → Years
* `365` → Days
* `2` → Highest & Lowest temperature

### Common Uses

* Time-series data
* Natural Language Processing (NLP)

---

## 4D Tensor

Most commonly used for **batches of images** in Computer Vision.

### Example

* 40 RGB images
* Height = 800 pixels
* Width = 1200 pixels

```text
Shape = (40, 800, 1200, 3)
```

where:

* `40` → Images
* `800` → Height
* `1200` → Width
* `3` → RGB channels

> **Note:** Some libraries store the RGB channel before the height and width (channels-first), while others store it last (channels-last).

---

## 5D Tensor

Most commonly used for **video data**.

### Example

Suppose you have:

* 4 videos
* 60 seconds each
* 30 frames per second (FPS)
* Resolution = 480 × 720
* RGB images

Frames per video:

```text
60 × 30 = 1800 frames
```

Tensor shape:

```text
(4, 1800, 480, 720, 3)
```

where:

* `4` → Videos
* `1800` → Frames
* `480` → Height
* `720` → Width
* `3` → RGB channels

---

# Hierarchy

```text
0D Tensor → Scalar

1D Tensor → Collection of Scalars (Vector)

2D Tensor → Collection of Vectors (Matrix)

3D Tensor → Collection of Matrices

4D Tensor → Collection of 3D Tensors
           (commonly Image Batches)

5D Tensor → Collection of 4D Tensors
           (commonly Video Batches)
```

---

# Quick Revision

| Tensor | Also Called            | Shape Example        |
| ------ | ---------------------- | -------------------- |
| 0D     | Scalar                 | `()`                 |
| 1D     | Vector                 | `(3,)`               |
| 2D     | Matrix                 | `(2,3)`              |
| 3D     | Collection of Matrices | `(3,2,4)`            |
| 4D     | Batch of Images        | `(40,800,1200,3)`    |
| 5D     | Batch of Videos        | `(4,1800,480,720,3)` |

> **Remember:** A tensor is simply a multidimensional array. As the number of dimensions (rank) increases, tensors can represent more complex data structures such as images, videos, time-series, and text.
