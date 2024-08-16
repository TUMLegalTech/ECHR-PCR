NOTE: Dataset is available on Hugging Face at https://huggingface.co/datasets/RashidHaddad/ECTHR-PCR.

Official dataset for the paper "ECtHR-PCR: A Dataset for Precedent Understanding and Prior Case Retrieval in the European Court of Human Rights".

Dataset is provided as a json file. Each ECHR application number maps to a json object which includes:

{
    "facts": list of case fact sentences from the judgement document,
    "law": list of law section sentences from the judgement document,
    "date": publication date,
    "citations": list of cited application numbers as strings
}

Applications numbers are unique to an application, however some cases produced more than one judgement document if the case was raised to the Grand Chamber.
To mitigate potential conflicts in the citation mapping process during subsequent stages, we employ a strategy of creating distinct versions of these cases by appending a version number (letters A, B, ...) to each document, ensuring that they remain distinguishable by their application numbers.
