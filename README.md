# rag
this is a llm rag model include hierarchical indexing and document filter 
![image](https://github.com/arcticfox9195/rag/assets/101635872/c2ff329c-391f-48d2-94d6-85b0255047ad)
first we need to install the package that we will import and use later.
![image](https://github.com/arcticfox9195/rag/assets/101635872/ae98ec87-e8c4-46ff-a90d-f75ea51e70c0)

import python library we need 
![image](https://github.com/arcticfox9195/rag/assets/101635872/30e67a3d-5993-42b2-a4b3-193ec551f5cc)

use pinecone api key create and initialize index
![image](https://github.com/arcticfox9195/rag/assets/101635872/1622e833-30ad-482b-b30d-1e96a5030e41)

Download and set the embedding model
![image](https://github.com/arcticfox9195/rag/assets/101635872/895fa530-0a91-45ae-abdc-c2ff65f3a8c1)

load document we crawled from website and use hierarchical indexing sort and preprocessing the data.It can make use more efficient when searching query

![image](https://github.com/arcticfox9195/rag/assets/101635872/0ec50b4e-2eda-43c5-8508-7fbafc71bf39)
![image](https://github.com/arcticfox9195/rag/assets/101635872/61bb3a21-bb21-4b78-8572-56e7d236e372)

split text into chuck

![image](https://github.com/arcticfox9195/rag/assets/101635872/8f3f12fc-2ca2-4583-a4cc-c602f8452e7e)
set query and encode it into ndarray type.Then search the query from your pinecone index.

![image](https://github.com/arcticfox9195/rag/assets/101635872/20121523-0003-4d5d-9407-bc225db0f247)
![image](https://github.com/arcticfox9195/rag/assets/101635872/624c69a5-1738-47b0-b3a8-b2b889635d1e)
![image](https://github.com/arcticfox9195/rag/assets/101635872/a86cd791-f00e-4ed5-8cb1-0f39e29c37a2)

use numpy library, cohere api help us calculate the similarity between content vector and query. Reranking the data and select top 3 hit result

![image](https://github.com/arcticfox9195/rag/assets/101635872/70b9892a-74a7-4d22-9337-ef88a161d21a)

final step, connect to google api to use generative model and set prompt to model. Model anwser the question(query) according to top 3 hit data content .
