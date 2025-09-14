# Geometry as new modality

## Geometry as a Modality in Generative AI: Reshaping RAG and SFT Applications

**Yes, geometry and shape can absolutely be considered a distinct modality in Generative AI.** Just as text, images, and audio carry unique information, the spatial and structural data inherent in geometric forms provide a rich, non-linguistic and non-visual (in its raw format) source of information for AI models. The burgeoning field of geometric deep learning is a testament to this, focusing on developing neural networks that can understand and generate 3D shapes, point clouds, and other geometric data.

This opens up exciting possibilities for applying established techniques like Retrieval Augmented Generation (RAG) and Supervised Fine-Tuning (SFT) to this geometric modality, although it often requires creative approaches to data representation.

---

### Retrieval Augmented Generation (RAG) for Geometric Data

Retrieval Augmented Generation, which enhances generative models by retrieving relevant information from an external knowledge base, can be adapted for geometric data. The core principle remains the same: provide the model with contextually relevant examples to improve the quality and accuracy of its output.

A key example of this in a specialized domain is the **Rag2Mol** research, which applies RAG to the geometric data of molecules for structure-based drug design. In this approach, the model retrieves known molecular structures (a form of geometric data) to inform the generation of new, viable drug candidates.

For more general 3D shapes, a RAG system could be built by:

* **Creating a Database of Geometric Assets:** This would involve curating a collection of 3D models, each with associated metadata. This metadata could include textual descriptions, tags, or even functional properties.
* **Developing a Retrieval Mechanism:** When a user provides a prompt (e.g., "a modern armchair with wooden legs"), the RAG system would first search the database for 3D models that are semantically similar. This could be achieved by searching the textual metadata or by using more advanced techniques that can compare geometric properties directly.
* **Augmenting the Generation Process:** The retrieved 3D models, along with their metadata, are then fed into the generative model as context. This helps the model to understand the desired style, components, and overall form, leading to a more accurate and detailed generated shape.



---

### Supervised Fine-Tuning (SFT) with Geometric Data

Supervised Fine-Tuning is the process of further training a pre-trained model on a smaller, labeled dataset to adapt it to a specific task. This is also a viable and powerful approach for working with geometric data.

The research paper on **GeoCoder**, for instance, demonstrates the fine-tuning of a vision-language model to solve geometry problems. By training the model on a dataset of geometric diagrams and corresponding questions and answers, the model's ability to reason about spatial relationships is significantly improved.

In the context of 3D shape generation, SFT can be used to:

* **Specialize a Model's Style:** A general text-to-3D model could be fine-tuned on a curated dataset of, for example, gothic architecture. This would teach the model the specific geometric features and stylistic nuances of that architectural style.
* **Teach Specific Object Generation:** If you need a model that is highly proficient at generating a particular type of object, like a specific car model, you could fine-tune a base model on a dataset of 3D models of that car from various angles and with different features.

---

### Making Geometry Feasible: Representation is Key

The primary challenge in applying RAG and SFT to geometric data lies in representing the shapes in a format that large language models can process. Here are the primary approaches:

* **Textual Representation:** This is the most direct way to bridge the gap between the geometric and textual modalities. A 3D model can be described in natural language, detailing its components, materials, and style. For instance, a chair could be represented as: "A four-legged chair with a high back, a square seat, and armrests. The legs and frame are made of dark wood, and the seat and back are upholstered in green fabric." These descriptions can then be used for both retrieving relevant models in a RAG system and for fine-tuning a model to associate specific text with geometric outcomes.

* **Graph-Based Representations:** Complex 3D shapes can be represented as graphs, where nodes represent different parts of the object and edges represent their relationships and connections. This structured representation can be more powerful than plain text for capturing the intricate topology of an object. The concept of "GraphRAG" is an emerging area that could be highly applicable here.

* **API Calls and Specialized Tools:** A growing number of APIs and tools are becoming available that can translate between text or code and 3D shapes. For example, a generative model could be designed to output code in a language like Python that, when executed, generates a 3D model using a specific library. This programmatic approach allows for precise and complex geometric constructions. Several platforms are now offering "text-to-3D" generation APIs that handle the complex conversion process behind the scenes.

In conclusion, while text and images are the most common modalities for RAG and SFT, the application of these powerful techniques to geometric and shape data is a rapidly advancing frontier in Generative AI. By creatively representing geometric information, researchers and developers are unlocking new possibilities for generating and interacting with the three-dimensional world.

***

For a deeper dive into the intersection of geometric principles and AI, you may find this video insightful:

[Watch a discussion on Symmetry, scale, and science in AI](https://www.youtube.com/watch?v=c61MbiPxJt8)
http://googleusercontent.com/youtube_content/0

# Geometry as a Modality in Generative AI: Beyond Text and Images

Yes, **geometry and shape can indeed be considered distinct modalities** in multimodal AI systems, similar to how text, images, and audio represent different data types. Current research demonstrates that geometric data is not only feasible as a modality but is actively being explored through various approaches, including RAG systems and supervised fine-tuning methods specifically designed for 3D geometric data.

## Understanding Geometric Modalities

Geometric modalities encompass various 3D data representations that capture spatial structure and shape information:[1][2][3]

**Point Clouds**: Unordered sets of 3D coordinates representing object surfaces, commonly generated by LiDAR sensors and depth cameras.[4]

**Meshes**: Structured representations consisting of vertices, edges, and faces that explicitly capture both surface geometry and topology.[5][6]

**Signed Distance Functions (SDFs)**: Implicit surface representations that encode the distance from any point to the nearest surface, with negative values inside objects and positive values outside.[7][8][9]

**Voxel Grids**: 3D arrays that discretize space into regular cubic elements, analogous to pixels in 2D images.[10][11]

**Neural Implicit Surfaces**: Continuous geometric representations learned by neural networks that can encode complex 3D shapes.[12][13]

## RAG Systems for Geometric Data

Recent advances show that **RAG approaches can indeed be built on geometric data**. The development of Spatial-RAG demonstrates how geometric information can be integrated into retrieval-augmented systems:[14][15][16]

**Spatial-RAG Framework**: This system extends traditional RAG to handle geospatial reasoning by combining sparse spatial filtering with dense semantic matching, treating geometric relationships (points, polylines, polygons) as retrievable modalities.[14]

**Hybrid Spatial Retrieval**: The approach uses both structured spatial databases and semantic embeddings, enabling systems to reason over geometric constraints while maintaining textual understanding capabilities.[14]

**Graph-based RAG**: Knowledge graphs incorporating geometric relationships enable more sophisticated retrieval of shape-related information, moving beyond simple text-based retrieval to capture spatial dependencies.[16][17]

## Supervised Fine-Tuning with Geometric Data

Multiple research directions demonstrate that **SFT approaches work effectively with geometric modalities**:[18][19][20]

**Geometric Fine-tuning**: Studies show that pre-trained models can be fine-tuned on geometric data, with approaches like MeSa demonstrating how masked, geometric, and supervised pre-training can be combined for depth estimation and 3D understanding tasks.[18]

**Multi-modal Fine-tuning**: Methods like TAMM (TriAdapter Multi-Modal Learning) show how geometric 3D shape understanding can be enhanced through fine-tuning that combines visual and geometric modalities.[21]

**Foundation Model Fine-tuning**: Research indicates that large-scale 3D shape-generative foundation models can be fine-tuned for specific geometric tasks without catastrophic forgetting when proper techniques are employed.[22]

## Current Research Approaches

The field has developed several successful methodologies for treating geometry as a first-class modality:

### Deep Learning on Geometric Data

**PointNet and PointNet++**: These pioneering architectures directly process raw point clouds, demonstrating that neural networks can learn meaningful representations from unstructured geometric data.[4]

**MeshCNN and MeshNet**: These methods apply convolutional operations directly to mesh edges and faces, treating geometric connectivity as learnable features.[6][5]

**Geometric Deep Learning**: This broader framework leverages symmetries and geometric priors to learn from complex data represented by graphs or multidimensional points in non-Euclidean domains.[23][24]

### Foundation Models for 3D Shapes

Recent work shows that **large-scale foundation models trained on geometric data** can capture rich geometric priors across both global and local dimensions:[25][26][22]

**3D Shape Generation**: Models like DiT-3D demonstrate that transformer architectures can be adapted for 3D shape generation, operating directly on voxelized point clouds.[11][27]

**Shape Transformers**: These models use self-attention mechanisms to learn nonlinear spatial correlations for 3D shapes, offering topology-independent representations that can work across different mesh structures.[28]

**Weight Space Learning**: Recent research explores treating the weight space of 3D shape-generative models as a data modality itself, enabling fine-grained control over both global topology and local geometry.[22]

## Geometric Embeddings and Representations

The field has developed sophisticated methods for creating embeddings from geometric data:[29][30][31]

**Geometric Relational Embeddings**: These map relational geometric data as geometric objects that combine vector information suitable for machine learning with structured spatial reasoning capabilities.[30]

**Multi-modal Contrastive Learning**: Frameworks that combine 3D mesh data with 2D projected images enable more robust geometric feature learning through cross-modal relationships.[3]

**Neural Implicit Representations**: These continuous representations can encode complex geometric structures and support various downstream tasks including shape completion, interpolation, and modification.[8][7][12]

## Practical Implementation Considerations

While geometric modalities show great promise, there are important implementation considerations:

**Data Preprocessing**: Unlike text or images, geometric data often requires specialized preprocessing including normalization, sampling, and topological consistency checks.[10][14]

**Computational Complexity**: 3D geometric operations are typically more computationally intensive than 2D image processing, requiring careful optimization for practical deployment.[32][4]

**Representation Choice**: The choice of geometric representation (points, meshes, SDFs, etc.) significantly impacts both the learning approach and the types of operations that can be efficiently performed.[9][13]

## Integration with Traditional Modalities

Current research demonstrates effective integration of geometric modalities with traditional text and image modalities:[33][3][21]

**Cross-modal Learning**: Systems can learn correspondences between geometric shapes and textual descriptions, enabling applications like text-to-3D generation.[34][21]

**Visual-Geometric Fusion**: Multi-modal systems combine 2D visual information with 3D geometric understanding for enhanced scene comprehension.[2][25]

Rather than requiring conversion to textual representations or API calls, **geometry functions as a native modality** with its own specialized neural architectures and learning paradigms. This approach preserves the rich spatial relationships and topological information that would be lost in text-based representations, while enabling the full power of modern deep learning techniques to operate directly on geometric data structures.

The field is rapidly advancing, with increasing evidence that geometric modalities can achieve performance comparable to or exceeding traditional approaches while offering new capabilities for spatial reasoning and 3D understanding tasks that are fundamental to applications in robotics, autonomous systems, and immersive technologies.

[1](https://arxiv.org/abs/2406.04254)
[2](https://arxiv.org/abs/2406.10722)
[3](https://nia.nbt.edu.cn/PDF/52_3D_Shape_Analysis_via_Multi-modal_Contrastive_Learning.pdf)
[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC6806315/)
[5](https://ranahanocka.github.io/MeshCNN/)
[6](https://arxiv.org/abs/1811.11424)
[7](https://lingjie0206.github.io/papers/NeuS/)
[8](https://arxiv.org/abs/2106.10689)
[9](https://openaccess.thecvf.com/content_CVPR_2019/papers/Park_DeepSDF_Learning_Continuous_Signed_Distance_Functions_for_Shape_Representation_CVPR_2019_paper.pdf)
[10](https://www.mathworks.com/help/vision/ug/getting-started-with-deep-learning-using-point-clouds.html)
[11](https://arxiv.org/abs/2307.01831)
[12](https://arxiv.org/abs/2201.09636)
[13](https://openaccess.thecvf.com/content/CVPR2023/papers/Zhang_Towards_Unbiased_Volume_Rendering_of_Neural_Implicit_Surfaces_With_Geometry_CVPR_2023_paper.pdf)
[14](https://arxiv.org/html/2502.18470v4)
[15](https://www.chitika.com/mathematical-pdf-parsing-rag/)
[16](https://writer.com/product/graph-based-rag/)
[17](https://pub.towardsai.net/building-graph-rag-for-structured-and-unstructured-data-e6148bcbe9c9)
[18](https://proceedings.mlr.press/v243/khan24a/khan24a.pdf)
[19](https://www.sciencedirect.com/science/article/pii/S0097849324001286)
[20](https://www.sciencedirect.com/science/article/abs/pii/S0010448525001150)
[21](https://arxiv.org/abs/2402.18490)
[22](https://arxiv.org/html/2503.21830v1)
[23](https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2023.1256352/full)
[24](https://pmc.ncbi.nlm.nih.gov/articles/PMC10687447/)
[25](https://europe.naverlabs.com/research/3d-foundation-models/)
[26](https://www.physicsx.ai/newsroom/building-beyond-human-imagination-with-foundation-models-for-geometry-and-physics)
[27](https://dit-3d.github.io)
[28](https://studios.disneyresearch.com/2022/04/25/shape-transformers-topology-independent-3d-shape-models-using-transformers/)
[29](https://proceedings.neurips.cc/paper/2021/file/88d25099b103efd638163ecb40a55589-Paper.pdf)
[30](https://arxiv.org/abs/2304.11949)
[31](https://arxiv.org/abs/2505.12540)
[32](https://www.kellton.com/kellton-tech-blog/the-rise-of-multimodal-data-ai)
[33](https://smythos.com/developers/agent-integrations/multimodal-ai/)
[34](https://machinelearning.apple.com/research/3d-shape-tokenization)
[35](https://instn.cea.fr/en/these/genphi-3d-generative-ai-conditioned-by-geometry-structure-and-physics/)
[36](https://arxiv.org/abs/2111.13361)
[37](https://www.physicsx.ai/newsroom/shaping-innovation-the-evolution-of-geometry-in-modern-engineering)
[38](https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-is-multimodal-ai)
[39](http://www.diva-portal.org/smash/get/diva2:1888229/FULLTEXT01.pdf)
[40](https://www.ijimai.org/journal/sites/default/files/2024-02/ijimai8_5_7.pdf)
[41](https://www.sciencedirect.com/science/article/pii/S0925231217302576)
[42](https://deepmind.google/discover/blog/alphageometry-an-olympiad-level-ai-system-for-geometry/)
[43](https://www.sciopen.com/article/10.1007/s41095-022-0321-5)
[44](https://www.sciencedirect.com/science/article/pii/S209526352400147X)
[45](https://www.splunk.com/en_us/blog/learn/multimodal-ai.html)
[46](https://community.openai.com/t/constructive-solid-geometry-generative-free-form-ai/4959)
[47](https://pmc.ncbi.nlm.nih.gov/articles/PMC12239537/)
[48](https://arxiv.org/abs/2506.14681)
[49](https://www.pinecone.io/learn/series/rag/rerankers/)
[50](https://www.kaggle.com/general/555397)
[51](https://www.linkedin.com/posts/danielhanchen_heres-a-complete-guide-to-fine-tuning-llms-activity-7351251048226836480-Qa-z)
[52](https://community.openai.com/t/what-ontology-rag-and-graph-data-do-you-use-to-develop-intelligent-assistants/787860)
[53](https://arxiv.org/html/2508.16546v1)
[54](https://proceedings.mlr.press/v32/johansson14.html)
[55](https://openreview.net/forum?id=19kqoNoc2N)
[56](https://github.com/iMoonLab/MeshNet)
[57](https://www.youtube.com/watch?v=gm_oW0bdzHs)
[58](https://sketchfab.com/VAA)
[59](https://arxiv.org/abs/2405.11903)
[60](https://arxiv.org/abs/2402.04821)
[61](https://3dfm.github.io)
[62](https://arxiv.org/abs/2311.02608)
[63](https://www.sciencedirect.com/science/article/pii/S0010482524004128)
[64](https://pro.arcgis.com/en/pro-app/3.4/help/data/las-dataset/introduction-to-deep-learning-and-point-clouds.htm)
[65](https://dl.acm.org/doi/10.1609/aaai.v33i01.33018279)
[66](http://stanford.edu/~rqi/pointnet/docs/cvpr17_pointnet_slides.pdf)
[67](https://sketchfab.com/VAA/models)
[68](http://proceedings.mlr.press/v139/ma21b/ma21b.pdf)
[69](https://light.princeton.edu/publication/gensdf/)
[70](https://www.youtube.com/watch?v=ZowE7-TeGKo)
[71](https://arxiv.org/abs/2011.13495)
[72](https://dsilvavinicius.github.io/nise/)
[73](https://cdwj.github.io/files/NNDL_Project_Final_Report.pdf)
[74](https://arxiv.org/abs/2309.12594)
[75](https://dl.acm.org/doi/10.5555/3540261.3542342)
[76](https://www.sciencedirect.com/science/article/pii/S0021999125004619)
[77](https://www.sciencedirect.com/science/article/pii/S0167839625000299)
[78](https://www.sciencedirect.com/science/article/pii/S0167839625000263)
[79](https://papers.neurips.cc/paper_files/paper/2020/file/731c83db8d2ff01bdc000083fd3c3740-Paper.pdf)