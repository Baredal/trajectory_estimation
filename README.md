# Drone Trajectory Estimation

Trajectory estimation from a sequence of aerial images and visualizes it on a global map using.

## Basis solution
The task was solved using **feature matching and homography-based transformations**.

It includes:
1. **Keypoints detection** in both drone and map images using SIFT.
2. **Matching features** using FLANN-based matcher.
3. Filtering matches using **Lowe's ratio test** to have only reliable correspondences.
4. Estimating the **homography transformation** using RANSAC to align with drone image to the map.
5. Computing **center location** of the drone that corresponds to genreal map coordinates from transformed image corners.
6. Accumulating all drone locations and **smoothing the trajectory** using cubic spline interpolation.
7. **Displaying the trajectory** on the general map.

---

## 🔧 Requirements

- Python 3.10+

Install dependencies:
```bash
pip install -r requirements.txt
```
After that you can download notebook and walkthrough (optionally you can run it by yourself but follow instructions in comments).
