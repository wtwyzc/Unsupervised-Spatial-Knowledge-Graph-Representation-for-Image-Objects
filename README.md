# Unsupervised-Spatial-Knowledge-Graph-Representation-for-Image-Objects
- Based on the derivative tool of large language model, i create an efficient flow：【Image ➡️ natural language ➡️ Knowledge map】
- The whole process does not require any annotation, and the generated knowledge graph can be interactive based on natural language. (Traditional knowledge graph requires a lot of manual annotation, entity extraction, relationship extraction, neo4j...)

## Basics
  - LISA（https://github.com/dvlab-research/LISA）：a segmentation inference model based on a large language model
  - LlamaIndex（https://github.com/run-llama/llama_index）：a data framework for large-scale language model

## prerequisite
  - OpenAI token
  - docker
  - NebulaGraph

## procedure（example）
1. First, the object detection API is used to identify objects in all images, and the image data set containing the computer is extracted
2. LISA traverses the image dataset, splits and returns a natural language description of the computer's location
3. Transform multiple computer location descriptions into a knowledge graph with the help of the LlamaIndex and NebulaGraph graph database
