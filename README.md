# 🎵 Music Recommendation System using Weaviate

A content-based music recommendation system built using Weaviate vector database, inspired by learnings from Retrieval-Augmented Generation (RAG) and vector search concepts.
The system recommends songs similar to a given input song based on audio features and metadata.

⸻

🚀 Project Overview

Traditional recommendation systems often rely on keywords or collaborative filtering.
This project explores a vector-based approach where each song is represented as a numerical embedding derived from its audio attributes.

Using Weaviate, the system performs fast Approximate Nearest Neighbour (ANN) searches to identify musically similar tracks.

⸻

🧠 Key Concepts Used
	•	Vector Databases & Embeddings
	•	Retrieval-Augmented Generation (RAG) concepts
	•	Semantic similarity search
	•	Approximate Nearest Neighbour (ANN) indexing
	•	Metadata-based filtering
	•	Content-based recommendation systems

⸻

📊 Data Source

The dataset is based on Spotify-style audio features, containing numerical attributes such as:
	•	danceability
	•	energy
	•	tempo
	•	valence
	•	acousticness
	•	loudness
	•	speechiness

These features naturally form dense vectors suitable for similarity search.

⸻

🧬 Song Embeddings

Instead of using a text-based vectorizer, this project uses a Bring Your Own Vector (BYOV) approach:
	•	Each song’s embedding is a vector composed of its audio features
	•	Weaviate is used purely for storage, indexing, and retrieval
	•	This provides full control and explainability over the recommendation logic

⸻

🗄️ Why Weaviate?

Weaviate was chosen because it offers:
	•	High-performance vector similarity search
	•	Support for ANN algorithms
	•	Flexible schema design
	•	Metadata filtering alongside vector search
	•	Native Python client
	•	Easy scalability for future multimodal extensions (lyrics, metadata, etc.)

⸻

⚡ Performance Optimizations
	•	Batch insertion of song records for faster ingestion
	•	Efficient schema design to minimize payload size
	•	Vector-only search for low-latency recommendations
	•	Ability to scale to large music libraries

⸻

🔍 Recommendation Logic
	1.	User provides a song title
	2.	The system retrieves the song’s vector
	3.	A near_vector query is executed in Weaviate
	4.	The top-K most similar songs are returned
	5.	The query song itself is excluded from the results

⸻

🛠️ Tech Stack
	•	Python
	•	Weaviate (Vector Database)
	•	Pandas, NumPy
	•	Docker (for local Weaviate instance)
	•	Spotify-style audio feature dataset

⸻

📌 Future Enhancements
	•	Hybrid search (vector + keyword)
	•	Genre and mood-based filtering
	•	Lyrics-based embeddings
	•	User personalization
	•	Evaluation metrics (Precision@K, Recall@K)
	•	UI or API layer

⸻

🎧 Motivation

This project combines my interest in music with modern AI retrieval systems.
It was built as a hands-on application of RAG and vector database concepts learned through DeepLearning.AI courses.

⸻

📬 Feedback & Contributions

Suggestions, improvements, and ideas are always welcome!
Feel free to open an issue or submit a pull request.

⸻

⭐ If you found this project interesting, consider giving it a star!
