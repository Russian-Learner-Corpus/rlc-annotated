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
- **id:** The sentence ID of the form **document_id**XXX, where XXX is the three-digit number of the sentence within the document.
- **document_id:** The ID of the document containing the sentence.
- **sentence_index:** The number of the sentence within the document.
- **text:** The original sentence.
- **corrected:** The corrected sentence.
- **status:** _needs correction_ if it is known that the corrected sentence is not quite right; empty, otherwise.

`annotations.csv`
- **id:** The error annotation ID.
- **sentence_id:** The ID of the sentence to which the annotation applies.
- **tag:** The error type.
- **quote:** The fragment containg an error.
- **correction:** The corrected fragment.
- **start:** The start offset of the original fragment within the sentence (indices refer to spaces between tokens; the start of the sentence has zero index).
- **end:** The end offset of the original fragment within the sentence (indices refer to spaces between tokens; the start of the sentence has zero index).
- **annotation_source:** _manual_ if annotation is entered by a person; _rlc-errant_ if the entire sentence was corrected by a person, but the edits were autmatically extracted and annotated by RLC-ERRANT.
