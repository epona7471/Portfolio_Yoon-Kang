ASR(Automatic Speech Recognition) STT model for Korean-accented English using Wav2vec2.0
=============

![image](https://user-images.githubusercontent.com/13134929/134042337-f0d85334-a24e-4595-88cb-1377a35433d0.png)

  This Model follows the template of hugging face's 'Fine-Tune Wav2Vec2 for English ASR with 🤗 Transformers' tutorial'([Link](https://huggingface.co/blog/fine-tune-wav2vec2-english)). In this case, this application is specialized in Speech recognition of Korean-accented English. Below comparisons in this page proves that same Wav2vec2.0 model trained by different accent datasets, resulting in its own unique performance. 

## 1. Dataset

1)  Korean-accented English speech dataset   
This Korean-english speech dataset is from https://aiopen.etri.re.kr/ (site's language only supports Korean), open data API service by ETRI(Electronics and Telecommunications Research Institute) from Korea. This datase contains .pcm recording files of 50 Korean native people reading 100 english sentences each, and its matching script.   
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
- base : Facebook's Wav2Vec2 base-model (https://huggingface.co/facebook/wav2vec2-base)
- Korean-English : Base + fine-tuned at Korean-English Dataset(approximately 5 hours)
- TIMIT : Base + fine-tuned at TIMIT Dataset(approximately 5 hours)
- 960h-lv60 :The large model pretrained and fine-tuned on 960 hours of Libri-Light and Librispeech on 16kHz sampled speech audio.

2) Model performance

|(All models have same base)|TIMIT test dataset(WER)|Korean-English test dataset(WER)|
|------|---|---|
|Korean-English|0.428|**0.16**|
|TIMIT|**0.186**|0.528|
|960h-lv60|**0.115**|0.368|
|TIMIT + Korean-English|0.285|**0.151**|

3) prediction samples
![image](https://user-images.githubusercontent.com/13134929/134122600-492036de-26e4-4f55-82fe-f20b2174bbfd.png)


## 3. Conclusion
  This model is a little bit behind from Wav2Vec2.0's SotA performance, since the model does not include LM(Language Model), and only functioning as character-based encoding-decoding model. However, regardless of the model's general performance, English speeches have some distinct attributes based on speaker's original accent, those should be considered when training and building ASR system.  
