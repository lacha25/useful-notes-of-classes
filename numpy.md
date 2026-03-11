# NumPy

## Arrays

- The main object is `ndarray`.
- Useful attributes:
  - `.shape`
  - `.ndim` for axis count
  - `.size` for number of elements
  - `.dtype` for element type
  - `.itemsize` for bytes per element
- Slicing returns a view, not a copy.

## Array Creation

- `np.array([...])`
- `np.asarray(a)` to convert
- `np.zeros(shape)`
- `np.ones(shape)`
- `np.empty(shape)` for faster initialization
- `np.full(shape, value)`
- `np.arange(start, stop, step)`
- `np.linspace(start, stop, number)`
- `np.eye(N)`

## Reshaping and Combining

- `a.reshape(shape)`
- `a.ravel()` flattens as a view
- `a.flatten()` flattens as a copy
- `a.T` transposes
- `np.concatenate(seq, axis=...)`
- `np.hstack(seq)`
- `np.vstack(seq)`
- `np.squeeze(a)` removes size-1 axes
- `np.stack(seq, axis=...)` joins along a new axis
- `np.clip(a, min, max)`

## Indexing and Selection

- `a[i:j]` slice view
- `a[:, i]` whole column view
- `a[mask]` boolean filter copy
- `a[idx]` fancy indexing copy

## Aggregation

- `np.sum(a)`
- `np.mean(a)`
- `np.std(a)`
- `np.min(a)`
- `np.argmin(a)` gives the index of the minimum
- `np.sort(a)` returns a sorted copy
- `a.sort()` sorts in place

## Linear Algebra and I/O

- `A @ B` for matrix multiplication
- `np.linalg.inv(a)`
- `np.linalg.solve(a, b)`
- `np.save(file, arr)` for `.npy`
- `np.load(file)` for `.npy` or `.npz`
- `np.loadtxt(fname)`

## Broadcasting

- Broadcasting works when shapes are compatible or when combining with a scalar.
