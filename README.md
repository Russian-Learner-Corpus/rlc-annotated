# Annotated RLC dataset

A partial dump of the  [Russian Learner Corpus](http://web-corpora.net/RLC) (RLC) consisting of corrected and annotated texts written by Russian learners

## Format

`documents.csv`
- **id:** The document ID.
- **subcorpus:** The subcorpus of RLC containing the document.
- **native:** The native laguage of the author.
- **language_background:** L2 speaker (FL) or heritage speaker (HL).
- **level:** Language level of the author.
- **words:** The number of words in the document.
- **sentences:** The number of sentences in the document.

`sentences.csv`
- **id:** The sentence ID of the form <document id>XXX, where XXX is the number of the sentence within the document.
- **document_id:** The ID of the document containing the sentence.
- **sentence_index:** The number of the sentence within the document.
- **text:** The original sentence.
- **corrected:** The corrected sentence.
- **status:** ``needs correction'' if it is known that the corrected sentence is not quite right; empty, otherwise.
