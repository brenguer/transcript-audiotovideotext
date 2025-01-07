## Transcrição de Vídeos do YouTube (Projeto de Aprendizado)

Este código é um script em Python que criei para transcrever áudio de vídeos do YouTube com fins de aprendizado. Ele utiliza o poderoso modelo de reconhecimento de fala Whisper, da OpenAI. 

**Como funciona:**

1. **Extração de Áudio:**  
   O script primeiro extrai a trilha de áudio do arquivo de vídeo fornecido usando a biblioteca `moviepy`.

2. **Configuração do Modelo:**  
    - Define o dispositivo de execução (GPU ou CPU) com base na disponibilidade.  
    - Carrega o modelo Whisper pré-treinado (`openai/whisper-large-v3`) e o configura para eficiência.  
    - Inicializa um pipeline de reconhecimento de fala utilizando o modelo e o processador.

3. **Transcrição:**  
    - Simula o processo carregando um clipe de áudio de exemplo do conjunto de dados Librispeech.  
    - Realiza o reconhecimento de fala no caminho de áudio fornecido (`PATHAUDIO`) e define o idioma para português no resultado.

4. **Salvando a Transcrição:**  
    - Por fim, extrai o texto transcrito e o salva no arquivo especificado (`PATH.txt`) com codificação UTF-8.

**Nota:**  

- Substitua `"PATH"` pelos caminhos reais dos seus arquivos de vídeo, áudio extraído e transcrição desejada.  
- Este é um projeto de aprendizado e pode exigir ajustes adicionais, dependendo do formato específico do seu vídeo e das funcionalidades desejadas.  

**Bibliotecas Utilizadas:**  

- `torch`: Framework de aprendizado profundo  
- `transformers`: Fornece modelos pré-treinados para diversas tarefas, incluindo reconhecimento de fala  
- `datasets`: Biblioteca para gerenciamento de conjuntos de dados  
- `moviepy`: Para edição de vídeos e extração de áudio  