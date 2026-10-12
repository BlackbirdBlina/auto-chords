# AutoChords

AutoChords tem por objetivo extrair a letra e a cifra de músicas de maneira automática, mesmo que seja uma música inédita.

## Modelos utlizados:
- [Whisper](https://huggingface.co/openai/whisper-large-v3-turbo)
- [SheetSage2](https://huggingface.co/m-a-p/SheetSage2)

## Setup

É necessário ter instalada a versão `3.11` do python:

    pyenv install 3.11

Além disso, como dependências é importante instalar, com atenção especial para a biblioteca `transformers` que precisa estar na versão `4.57.6`:

    pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/rocm7.2
    pip install openai-whisper
    pip install "transformers==4.57.6"
    pip install accelerate
    pip install mir_eval 
    pip install protobuf
    pip install pretty_midi
    
Como dependência do sistema:

    sudo apt install ffmpeg

Para ajudar na precisão da letra foi utilizada a biblioteca `demucs` que separa os instrumentos da voz:

    pip install -U demucs


## Importante

O projeto possui limitações devido às bibliotecas utilizadas, então pode haver inconsistências na captura dos dados.