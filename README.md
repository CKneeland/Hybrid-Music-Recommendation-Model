# Hybrid-Music-Recommendation-Model

Final Paper Link: https://docs.google.com/document/d/1pb6EcHczJq8Y0WVEP30b0bEAZSwG0g7x68_DCrLt8RM/edit?usp=sharing

**This repository contains the files for Connor Kneeland and John Sterns final project submission.**

The files called `Spotify API to MongoDB` and `Neo4j Data Pipeline` contain the code for querying data from the Spotify API, pre-processing the data, and loading it into the Neo4j graph database with relationships. When run, the Spotify API to MongoDB grabs music data as needed, and should be run first to get new data. The Neo4j Data Pipeline would be run second and takes the collected data from MongoDB, pre-processes it, and uploads track and playlist nodes to Neo4j. After that, it then creates all the relationships between nodes. These files take a long time to run.

To run these files, the following packages will be needed:
- `pymongo`
- `py2neo`
- `numpy`
- `sklearn`

The file called `Hybrid (CF and CBF) Recommendation Model` queries all nodes and relationships from the graph database, and when given a playlist to make recommendations with, returns the top k recommendations. 

To run this file, the following packages will be needed:
- `py2neo`
- `numpy`
- `heapq`
- `collections`
- `spotipy`

The file called `Hybrid Recommendation Model Evaluation` runs similar to the actual recommendation model, but is used to provide evaluation metrics on the recommendations themselves.
