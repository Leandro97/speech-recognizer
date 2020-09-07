# speech-recognizer

## Getting requeriments
Before running the notebook get the requeriments. Run the following command in the prject folder

pip install -r requeriments.txt

## Getting the data
After installing the requeriments run the following commands in the project folder

wget http://www.openslr.org/resources/12/dev-clean.tar.gz
tar -xzvf dev-clean.tar.gz

wget http://www.openslr.org/resources/12/test-clean.tar.gz
tar -xzvf test-clean.tar.gz

mv flac_to_wav.sh LibriSpeech
cd LibriSpeech
./flac_to_wav.sh

     
cd ..
python create_desc_json.py LibriSpeech/dev-clean/ train_corpus.json
python create_desc_json.py LibriSpeech/test-clean/ valid_corpus.json

## Presentation script
https://docs.google.com/document/d/1RgDw9on_WAeryO0PhHRUM5MQnBsQrgjQ0MTWVJn_jXY