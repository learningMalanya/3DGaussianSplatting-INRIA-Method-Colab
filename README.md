# **3DGaussianSplatting-INRIA-Method-Colab**  

Welcome to a Colab-friendly setup for INRIA’s groundbreaking **3D Gaussian Splatting** method! This repository makes real-time radiance field rendering accessible on Google Colab by addressing version mismatches and GPU compatibility issues.  

## **What’s This About?**  
INRIA’s **3D Gaussian Splatting** ([graphdeco-inria/gaussian-splatting](https://github.com/graphdeco-inria/gaussian-splatting)) is a game-changer for turning 2D photos into fast, photorealistic 3D scenes. Running it in Colab was made easier thanks to **camenduru’s August 2023 template**, which provided a great starting point. However, with evolving Colab environments, some dependencies changed, leading to issues such as:  

> **Error:** `"subprocess-exited-with-error × python setup.py bdist_wheel did not run successfully."`  

To restore smooth functionality, I adapted camenduru’s approach, resolving version mismatches and updating dependencies in this notebook.  

- **Original Repo**: [graphdeco-inria/gaussian-splatting](https://github.com/graphdeco-inria/gaussian-splatting)  
- **Inspired By**: [camenduru’s Colab template (August 2023)](https://github.com/camenduru)  
- **Notebook**: [3DGaussianSplatting_INRIA_Method_Colab.ipynb](3DGaussianSplatting_INRIA_Method_Colab.ipynb)  

## **What’s Updated?**  
Colab’s default setup (Python 3.11, CUDA 12.4, PyTorch 2.x) no longer aligns with INRIA’s original environment. To ensure compatibility on a **Tesla T4**, I made the following adjustments:  

- **Python 3.7** → Downgraded to match `environment.yml` (3.7.13) for stability.  
- **CUDA 11.8 Toolkit** → Installed to bridge Colab’s 12.4 drivers with compatibility magic.  
- **PyTorch 1.12.1+cu116** → Aligned with `environment.yml`, ensuring CUDA compatibility.  
- **Environment Tweaks** → Adjusted `PATH` and `LD_LIBRARY_PATH` for smooth GPU execution.  

With these fixes, the notebook **trains successfully** and **renders 3D scenes** in Colab!  

## **How to Use It**  
1. Open [3DGaussianSplatting_INRIA_Method_Colab.ipynb](3DGaussianSplatting_INRIA_Method_Colab.ipynb) in Colab.  
2. Run all cells—this will install dependencies, train on the **Tanks & Temples dataset** (`tandt_db.zip`), and render images.  
3. Check `/content/gaussian-splatting/output/[random_id]/` for your `.ply` and rendered PNGs (`train/` or `test/`).  

## **What You’ll See**  
- **Training** → Builds 3D Gaussians from photos (this takes time—grab a coffee!).  
- **Rendering** → Converts Gaussians into photorealistic images—compare `gt/` (real photos) with `renders/` (synthetic views).  

## **Try It Out!**  
Fire up the notebook and let me know how it goes! If you encounter issues or have suggestions, feel free to **open an issue or PR**. Your feedback is welcome!  

## **Credits**  
- **INRIA Team** → For the cutting-edge **3D Gaussian Splatting** method.  
- **camenduru** → For the original **Colab template**, which worked well in August 2023 and provided a strong foundation.  
- **Colab Community** → For ongoing insights into GPU and environment quirks.  

**Happy splatting!** 🎨🚀  
