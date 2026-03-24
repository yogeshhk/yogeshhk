# Geometric AI Consultancy Guide
### Domain: Graph Transformers · Point Cloud · Mesh CNN · Geometric Deep Learning

---

## Table of Contents
1. [Market Fit](#1-market-fit)
2. [Portfolio Problems](#2-portfolio-problems)
3. [Tech Stack](#3-tech-stack)
4. [Roadmap](#4-roadmap)
5. [Business Strategy — 10 Years](#5-business-strategy--10-years)

---

## 1. Market Fit

### Domain Verdict
**✓ Strong niche — undercrowded, high-value (Emerging)**

Deep geometry AI skills are rare. Demand grows faster than supply across AEC, automotive, robotics, and medical imaging.

### Industry Demand by Sector

| Sector | Demand Signal |
|---|---|
| Autonomous vehicles | 95% |
| Medical imaging 3D | 90% |
| Robotics / grasping | 85% |
| AEC (BIM/scan-to-BIM) | 80% |
| Industrial NDT / inspection | 75% |
| Game / VFX / 3D generation | 65% |

### Salary Benchmarks

| Role | India (LPA) | Remote USD |
|---|---|---|
| 3D Deep Learning Engineer | ₹18–32L | $90–140k |
| GDL Research Engineer | ₹25–45L | $120–180k |
| Point cloud consultant | ₹30–60L | $140–200k |
| Freelance project rate | — | $100–200/hr |

### Risk Factors

**Slow enterprise sales cycles** *(Mitigate)*
AEC & automotive deals take 6–18 months. Offset with faster robotics/startup clients.

**Hardware dependency** *(Plan for)*
Clients need LiDAR, RGBD, or CT hardware. Become hardware-agnostic and support simulation fallback.

---

## 2. Portfolio Problems

### Tier 1 — Core Showcase (build all 3)

**1. LiDAR defect detector** `High signal`
Segmentation + anomaly detection on real industrial scan data (KITTI or ModelNet). PointNet++ backbone, PyG. Shows end-to-end production thinking.

**2. 3D medical structure segmentation** `High signal`
Organ/lesion segmentation on CT/MRI point cloud or mesh (use MedShapeNet or ShapeNet). Mesh CNN + graph transformer. Clients pay premium here.

**3. Multi-modal 1D+3D fusion** `Differentiator`
Fuse vibration sensor (1D) + depth camera (3D) for predictive maintenance. GNN over heterogeneous graph. Exactly the "unified framework across dimensions" thesis — no pure 2D CNN specialist can claim this.

### Tier 2 — Breadth Signal (pick 2)

**4. Scene graph from point cloud** `Robotics`
Detect objects, build spatial relationship graph, answer "is box A on top of B?" — GNN on scene graph. Great for robotics clients.

**5. Mesh simplification with quality preservation**
GDL-guided decimation for game/VFX. Use PyMeshLab + custom GNN loss. Rare skill, niche but lucrative.

**6. Few-shot 3D shape classification** `Research edge`
Prototypical networks on ShapeNet embeddings. Demonstrates graph transformer + meta-learning. Positions you for research consulting.

### Publish Format for Each Project

For every project, build this credibility chain:

```
GitHub repo → Weights & Biases run → 3-min video demo → arXiv/blog writeup → Hugging Face Space (interactive)
```

---

## 3. Tech Stack

### Core (must master)

| Library | Purpose |
|---|---|
| **PyTorch + PyG** | PyTorch Geometric — primary GNN framework. MessagePassing, DataLoader, transforms. No shortcut here. |
| **Open3D** | Point cloud I/O, voxel grid, ICP, normal estimation. Replaces PCL for most Python workflows. |
| **PointNet / PointNet++** | Foundational architecture. Implement from scratch once; use PyG's built-in version in production. |
| **Mesh CNN / DiffusionNet** | For triangle mesh inputs. DiffusionNet (2022) is current SOTA — more robust than MeshCNN. |

### Modern / Emerging (competitive edge)

| Library | Why |
|---|---|
| **Point Transformer v3** *(2024)* | Best accuracy on ScanNet/S3DIS. Attention on local neighborhoods. Know the architecture deeply. |
| **3D Gaussian Splatting** *(Booming)* | Fastest-growing 3D representation. Bridges graphics and ML. High client interest in AEC and digital twins. |
| **MinkowskiEngine / TorchSparse** | Sparse 3D convolutions for large outdoor scans. Essential for autonomous driving projects. |
| **Kaolin (NVIDIA)** | 3D deep learning ops, differentiable rendering. Useful for generative 3D model work. |

### Supporting Stack

`NumPy / SciPy` · `trimesh` · `PyMeshLab` · `PDAL (LiDAR pipelines)` · `Weights & Biases` · `ONNX export` · `TorchScript` · `FastAPI (serving)` · `Docker` · `CUDA basics` · `ROS 2 (robotics)` · `ITK (medical)`

### Skip or Deprioritize

**PCL (C++ library)**
Useful for embedded/ROS work but not needed for consultancy. Open3D covers 90% of use cases in Python.

**VTK directly**
ITK/Open3D wrap it. Only dive into raw VTK for medical imaging edge cases.

---

## 4. Roadmap

### Month 0–3 — Foundations
Master PyTorch Geometric. Implement PointNet++ and a basic GNN from scratch. Complete ShapeNet classification project. Set up GitHub + W&B portfolio infrastructure.

### Month 3–6 — Specialization
Build Tier 1 projects (LiDAR defect, medical segmentation). Publish 2 blog posts. Submit 1 paper to a workshop (CVPR/ICCV workshops accept applied work). First LinkedIn presence as "geometric AI specialist".

### Month 6–12 — First Clients
Target 2–3 paid projects: Upwork/Toptal for quick wins, cold outreach to AEC/robotics startups. Price at ₹8–15k/day. Validate one vertical deeply (e.g. AEC or medical). Build a micro-tool (paid or free) and release it.

### Year 1–2 — Consultancy Formation
Register firm. 3–5 active clients. Hire 1 junior. Begin productizing: a reusable SDK/pipeline component. Speak at a regional ML conference.

**Revenue target: ₹30–50L annual**

### Year 2–4 — Vertical Depth
Pick one vertical (AEC, medical, automotive) and become the go-to name in India for it. Retainer contracts. Co-author with academia.

**Revenue target: ₹1–2 Cr ARR**

### Year 4–10 — Scale or Productize
Three strategic options:

- **Option A:** Scale agency — 5–10 person boutique, global clients
- **Option B:** Spin out a SaaS product (e.g. plug-and-play 3D inspection API)
- **Option C:** Research + consulting hybrid (IITB/IITM partnership)

**Revenue target: ₹3–10 Cr ARR**

---

## 5. Business Strategy — 10 Years

### Positioning Strategy

**Choose a vertical anchor, not a technique anchor.**
Don't say "I do GNNs". Say "I build 3D inspection AI for manufacturing" or "geometry AI for AEC". Clients buy outcomes, not algorithms.

### Revenue Streams (layer over time)

| Stream | Timeline | Margin |
|---|---|---|
| Project consulting | Year 0–2 | High, low scale |
| Retainer / embedded | Year 1–3 | Predictable |
| Technical training / workshops | Year 1+ | 80%+ |
| Open-source + paid SDK | Year 2+ | Recurring |
| SaaS API (3D inspection) | Year 4+ | Best long-term |

### Things Most Consultants Miss

**IP ownership clause in every contract** *(Critical)*
Retain rights to reusable components. This lets you build a compounding library over 10 years.

**Academia pipeline** *(Underused)*
Co-supervise MTech/PhD students at IIT/IISc. Free R&D, talent pipeline, credibility, and publications.

**Niche community ownership**
Start/own an Indian "Geometric AI" Discord/newsletter. Distribution moat. Clients come to you. Start in year 1 even with 50 members — it compounds massively.

**Hardware agnosticism positioning**
Support RealSense, Velodyne, Matterport, FARO, phone LiDAR. Don't lock to one sensor vendor — clients love this.

**Watch: 3D Foundation Models** *(Next 3 years)*
UniPAD, Point-MAE, Uni3D — these will reshape the stack by 2027. Learn masked autoencoding for 3D now. Stay current or risk obsolescence.

---

## Key Takeaways

1. **Single most important early move:** Build the multi-modal 1D+3D fusion project. It directly demonstrates the "unified framework" thesis that no pure 2D CNN specialist can claim.
2. **Tech bet to make now:** Learn Point Transformer v3 + 3D Gaussian Splatting in parallel — current SOTA + highest demand growth.
3. **Biggest mistake to avoid:** Positioning around technique rather than outcome vertical. Pick one vertical in year one.
4. **10-year asymmetric bet:** Start a Geometric AI India community in year 1. Whoever owns the community owns the deal flow.

---

*Generated: March 2026 | Domain: Geometric Deep Learning · GNNs · Point Cloud · Mesh CNN*
