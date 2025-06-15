# Bulk Carrier Picture Shredder

A Python script inspired by the “dog breeder shredding” meme.  
Cuts an image into tiles, rotates columns, recombines rows and columns, and builds a collage to visually “prove we live in a simulation” using NumPy and PIL.

---

## Features
- Slices any image into a grid of tiles (rows × columns)
- Rotates every second column for a “simulation glitch” effect
- Recombines tiles using odd/even row and column logic
- Displays and combines all steps into a single collage
- All steps reproducible and configurable

---

## Demo Result
*(Include a small version of your collage image here if you want. Example:)*
![Sample Collage](collage.jpg)

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/tubrikas/bulk_carrier_shredder.git
cd YOUR_REPOSITORY
```

---

### 2. Place Your Image
- Place your input image (e.g., `bulk-carrier.jpg`) in the project folder.
- You can use any image, but high-resolution images look best.

---

### 3. Create a Virtual Environment (Recommended)
On **Windows**:
```bash
python -m venv venv
venv\Scripts\activate
```
On **Mac/Linux**:
```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 4. Install Requirements

```bash
pip install -r requirements.txt
```

**requirements.txt** example:
```
pillow==11.2.1
numpy==2.2.5
ipython==9.1.0
python==3.13.2
```

*(Add `matplotlib` if you want to save or show outside Jupyter.)*

---

## How to Run

- **In Jupyter Notebook or JupyterLab:**  
  Paste the script into a cell and run, or use a `.ipynb` notebook.

- **In Python Script (no Jupyter):**  
  Replace `display()` with `img.show()` for local preview, or save images with `img.save("output.jpg")`.

- **Set parameters** at the top:
  - `image_path = 'bulk-carrier.jpg'`
  - `num_rows, num_cols = 78, 100`

---

## How It Works (Step-by-step)

1. **Load image** using Pillow and convert to NumPy array.
2. **Split into tiles** by rows & columns.
3. **Rotate every odd column** by 90 degrees for “glitch” effect.
4. **Recombine**: 
    - First by rows (odd/even)
    - Then by columns (odd/even)
5. **Resize results** for the collage.
6. **Build collage** showing all steps.
7. **Display** each result (requires Jupyter/IPython for `display()`).

---
