![image](https://user-images.githubusercontent.com/13134929/134042337-f0d85334-a24e-4595-88cb-1377a35433d0.png)

 This Model follows the template of hugging face's 'Fine-Tune Wav2Vec2 for English ASR with 🤗 Transformers' tutorial'(Link). In this case, this application is specialized in Speech recognition of Korean-accented English. Below comparisons in this page proves that models each trained by datasets with different accents, resulting in its own unique performance. 

## 1. Dataset

1)  Korean-accented English speech dataset
This Korean-english speech dataset is from https://aiopen.etri.re.kr/(Site's language only supports Korean), open data API service by ETRI(Electronics and Telecommunications Research Institute) from Korea. This datase contains .pcm recording files of each 50 Korean native people reading 100 english sentences, and its matching transcriptions.   
You can find details from data-preprocess to training in the file **'Fine_tuning_Wav2Vec2_for_English_ASR_Korean-English.ipynb'**

2) Timit speech dataset (for the details : https://huggingface.co/datasets/timit_asr)   
You can find details from data-preprocess to training in the file **'Fine_tuning_Wav2Vec2_for_English_ASR_TIMIT.ipynb'**
``` 
   DatasetDict({
       train: Dataset({
           features: ['file', 'text', 'phonetic_detail', 'word_detail', 'dialect_region', 'sentence_type', 'speaker_id', 'id'],
           num_rows: 4620
       })
       test: Dataset({
           features: ['file', 'text', 'phonetic_detail', 'word_detail', 'dialect_region', 'sentence_type', 'speaker_id', 'id'],
           num_rows: 1680
       })
   })
```

## 2. Training results

1) Model description
a. base : Facebook's Wav2Vec2 base-model
