1) This code is designed to check the uniqueness and plagiarism percentage of a document compared to a reference text. It uses various Python libraries to extract the text from the file provided by the user, preprocess the text, and generate a TF-IDF matrix. The cosine similarity is then calculated between the document and reference text, and the percentages of uniqueness and plagiarism are calculated accordingly. Finally, the results are displayed in a graph.

2) Importing necessary libraries:
   os: used for system functions
   docx2txt: used for extracting text from .docx files
   PyPDF2: used for extracting text from .pdf files
   pptx: used for extracting text from .pptx files
   textract: used for extracting text from various file types
   CountVectorizer: used for generating the TF-IDF matrix
   cosine_similarity: used for calculating the cosine similarity
   matplotlib.pyplot: used for displaying the results in a graph                                                                                                         

3) Defining a preprocess function: Removes all non-alphanumeric characters from the text and Tokenizes the text.
4) Prompting the user for a file path: Asks the user to input the file path of the document to be checked.
5) Extracting text from the file:
   * If the file is a .txt file, the text is extracted using Python's built-in file handling functions
   * If the file is a .docx file, the text is extracted using the docx2txt library
   * If the file is a .pdf file, the text is extracted using the PyPDF2 library
   * If the file is a .pptx file, the text is extracted using the pptx library
   * If the file is a .doc file, it is converted to a .docx file using the unoconv library and then the text is extracted using the docx2txt library
   * For all other file types, the text is extracted using the textract library
6) Preprocessing the text: The text is preprocessed using the preprocess function defined earlier.
7) Prompting the user for reference text: Asks the user to input the reference text to be compared to the document.
8) Preprocessing the reference text: The reference text is preprocessed using the preprocess function defined earlier.
9) Generating the TF-IDF matrix: The CountVectorizer library is used to generate the TF-IDF matrix.
10) Calculating the cosine similarity: The cosine_similarity library is used to calculate the cosine similarity between the document and reference text.
11) Calculating the uniqueness and plagiarism percentages: The uniqueness percentage is calculated as 100 - (cosine similarity * 100) and The plagiarism percentage is calculated as cosine similarity * 100.
12) Displaying the results in a graph: A pie chart is generated using matplotlib.pyplot library,The chart displays the uniqueness and plagiarism percentages and The chart is displayed to the user
