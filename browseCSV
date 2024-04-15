#############
# DondoCorp #
#############
import os
import sys

from langchain.indexes import VectorstoreIndexCreator
from langchain_community.document_loaders import TextLoader
from sqlalchemy.engine import URL
from langchain_openai import OpenAIEmbeddings

os.environ["OPENAI_API_KEY"] = "x"

loader = TextLoader(sys.argv[2])
index = VectorstoreIndexCreator().from_loaders([loader])

query = sys.argv[1]

print(query)
print(index.query(query))
