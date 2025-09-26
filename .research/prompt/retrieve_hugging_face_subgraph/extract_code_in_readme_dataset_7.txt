
Input:
From the Hugging Face README provided in “# README,” extract and output only the Python code required for execution. Do not output any other information. In particular, if no implementation method is described, output an empty string.

# README
---
{}
---

# Dataset Card for Fashion-MNIST

<!-- Provide a quick summary of the dataset. -->

## Dataset Details

### Dataset Description

<!-- Provide a longer summary of what this dataset is. -->
Fashion-MNIST is a dataset of 70,000 grayscale images, each 28×28 pixels, representing 10 different classes of clothing and accessories. It serves as a drop-in replacement for the original MNIST dataset but provides a more challenging benchmark for machine learning models. The dataset was introduced by Zalando Research to address the limitations of MNIST, which primarily contains handwritten digits.

### Dataset Sources

<!-- Provide the basic links for the dataset. -->

- **Homepage:** https://github.com/zalandoresearch/fashion-mnist?tab=readme-ov-file#license
- **Paper:** Xiao, H., Rasul, K., & Vollgraf, R. (2017). Fashion-mnist: a novel image dataset for benchmarking machine learning algorithms. arXiv preprint arXiv:1708.07747.

## Dataset Structure

<!-- This section provides a description of the dataset fields, and additional information about the dataset structure such as criteria used to create the splits, relationships between data points, etc. -->

Total images: 70,000

Classes: 10 (T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot)

Splits:

- **Train:** 60,000 images

- **Test:** 10,000 images

Image specs: PNG format, 28×28 pixels, Grayscale

## Example Usage
Below is a quick example of how to load this dataset via the Hugging Face Datasets library.
```
from datasets import load_dataset  

# Load the dataset  
dataset = load_dataset("randall-lab/fashion-mnist", split="train", trust_remote_code=True)  
# dataset = load_dataset("randall-lab/fashion-mnist", split="test", trust_remote_code=True)  

# Access a sample from the dataset  
example = dataset[0]  
image = example["image"]  
label = example["label"]  

image.show()  # Display the image  
print(f"Label: {label}")
```

## Citation

<!-- If there is a paper or blog post introducing the dataset, the APA and Bibtex information for that should go in this section. -->

**BibTeX:**

@online{xiao2017/online,
  author       = {Han Xiao and Kashif Rasul and Roland Vollgraf},
  title        = {Fashion-MNIST: a Novel Image Dataset for Benchmarking Machine Learning Algorithms},
  date         = {2017-08-28},
  year         = {2017},
  eprintclass  = {cs.LG},
  eprinttype   = {arXiv},
  eprint       = {cs.LG/1708.07747},
}

Output:
{
    "extracted_code": "from datasets import load_dataset\n\n# Load the dataset\ndataset = load_dataset(\"randall-lab/fashion-mnist\", split=\"train\", trust_remote_code=True)\n# dataset = load_dataset(\"randall-lab/fashion-mnist\", split=\"test\", trust_remote_code=True)\n\n# Access a sample from the dataset\nexample = dataset[0]\nimage = example[\"image\"]\nlabel = example[\"label\"]\n\nimage.show()  # Display the image\nprint(f\"Label: {label}\")"
}
