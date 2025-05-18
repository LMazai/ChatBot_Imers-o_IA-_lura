# ChatBot_Imers-o_IA-_lura
# FriendlyEnglish - Chatbot de Ensino de Inglês para Telegram 🤖

**FriendlyEnglish** é um chatbot inteligente para Telegram projetado para ajudar falantes de português a praticar e aprender inglês de forma interativa e engajadora. Utilizando o poder da IA Generativa do Google (Gemini), o bot oferece correções, explicações, e mantém a conversa fluindo!

## Funcionalidades Principais ✨

*   **🧠 Inteligência Artificial com Gemini:** Respostas e interações geradas pelo modelo Gemini 1.5 Flash do Google, proporcionando conversas naturais e contextuais.
*   🗣️ **Interação por Voz e Texto:**
    *   Envie mensagens de texto ou áudio.
    *   O bot responde na mesma modalidade: texto por texto, voz por voz.
*   🌐 **Detecção Automática de Idioma (Português/Inglês):**
    *   **Perguntas em Português?** O bot responde em português, oferecendo traduções e explicações claras de como frases e palavras são usadas em inglês.
    *   **Prática em Inglês?** O bot responde em inglês, corrigindo erros gramaticais ou de vocabulário de forma didática e encorajadora.
*   🎙️ **Respostas em Áudio com Sotaque Contextualizado:**
    *   Partes de explicações em português que citam termos em inglês podem ter o áudio daquele termo em inglês com pronúncia nativa.
*   🚀 **Engajamento Contínuo:** O bot sempre tenta continuar a conversa após fornecer uma resposta, fazendo perguntas relevantes ou convidando o usuário a praticar mais.
*   🔔 **Lembretes Motivacionais em Áudio:**
    *   Mensagens de voz periódicas (entre 9h e 19h, fuso de Brasilia) em inglês para incentivar a prática regular.
    *   *Esta funcionalidade opera enquanto o script do bot estiver em execução (ex: no Google Colab).*
*   📝 **Respostas Concisas e Claras:** Foco em explicações e correções curtas e de fácil entendimento para aprendizes.

## Como Funciona (Tecnologias) 🛠️

*   **Plataforma:** Telegram
*   **Linguagem:** Python
*   **Biblioteca do Bot:** `python-telegram-bot` (assíncrona)
*   **IA Generativa:** Google Gemini 2.0 Flash API
*   **Reconhecimento de Fala (STT):** `SpeechRecognition` (com motor Google)
*   **Síntese de Fala (TTS):** `gTTS` (Google Text-to-Speech) para áudios mais naturais.
*   **Manipulação de Áudio:** `pydub` (com `ffmpeg`)

## Demonstração (Como Usar) ▶️

1.  Encontre o bot no Telegram (você precisará criar o seu e adicionar o token).
2.  Envie `/start` para iniciar a conversa.
3.  Converse naturalmente:
    *   Faça perguntas em português sobre como dizer algo em inglês.
    *   Pratique enviando frases ou mensagens de voz em inglês.
4.  O bot detectará o idioma e responderá apropriadamente, buscando sempre manter o diálogo.

*(Adicione aqui um GIF ou screenshots do bot em ação, se possível)*

## Configuração e Execução (Google Colab) ⚙️

Este projeto foi desenvolvido e testado primariamente no ambiente Google Colab.

1.  **Clone o Repositório (ou copie o código):**
    ```bash
    git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
    ```
2.  **Abra o Notebook no Google Colab.**
3.  **Configure as API Keys:**
    *   No Google Colab, acesse "Símbolos Secretos" (ícone de chave 🔑 no painel esquerdo).
    *   Adicione os seguintes símbolos secretos:
        *   `GOOGLE_API_KEY`: Sua chave da API do Google para o Gemini (obtenha em [Google AI Studio](https://aistudio.google.com/)).
        *   `TELEGRAM_BOT_TOKEN`: O token do seu bot do Telegram (obtenha com o @BotFather no Telegram).
4.  **Execute as Células:** Execute as células do notebook em ordem.
    *   A primeira célula instalará as dependências.
    *   As células seguintes definem a lógica do bot.
    *   A última célula iniciará o bot. Ele permanecerá ativo enquanto a célula estiver rodando e o Colab conectado.

## Para Desenvolvedores 🧑‍💻

*   **Estrutura do Código:**
    *   `Célula 2`: Instalações e configuração das chaves.
    *   `Célula 3`: Lógica principal de interação com a API Gemini e as funções de STT/TTS.
    *   `Célula 4`: Definição dos handlers do Telegram (comandos, mensagens de texto/voz) e a tarefa de agendamento dos lembretes.
    *   `Célula 5`: Script para iniciar e rodar o bot.
*   **Personalização:**
    *   Ajuste os prompts na função `get_gemini_response_v4` para refinar o comportamento e o "tom" do bot.
    *   Modifique as mensagens em `reminder_messages_audio_en_v4`.
    *   Experimente com diferentes parâmetros do Gemini (temperatura, `max_output_tokens`).

## Atualizações Futuras Planejadas (Roadmap) 🗺️

Estamos sempre buscando melhorar o English Buddy! Algumas ideias para o futuro incluem:

*   📊 **Acompanhamento de Progresso (Simples):** Implementar uma forma básica de o usuário ver estatísticas simples de sua interação.
*   🎯 **Exercícios Direcionados:** Adicionar comandos para tipos específicos de prática (ex: completar frases, identificar tempos verbais).
*   🗣️ **Avaliação de Pronúncia (Avançado):** Integrar ferramentas mais sofisticadas para feedback sobre a pronúncia do usuário (desafiador e pode requerer APIs pagas).
*   📱 **Expansão para Outras Plataformas:**
    *   **WhatsApp:** Explorar a integração via API oficial do WhatsApp Business (nota: requer aprovação e pode ter custos associados).
    *   **Discord:** Adaptar o bot para funcionar em servidores Discord.
*   🌐 **Hospedagem Persistente:** Mover o bot do Google Colab para uma plataforma de hospedagem que permita execução 24/7 (ex: Heroku, PythonAnywhere, AWS, Google Cloud).
*   📚 **Base de Conhecimento Aprimorada:** Permitir que o bot consulte materiais de estudo específicos ou FAQs.

## Contribuições 🤝

Contribuições são bem-vindas! Se você tem ideias para novas funcionalidades, melhorias ou correções de bugs, sinta-se à vontade para abrir uma *Issue* ou enviar um *Pull Request*.

## Licença 📄

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes (você precisará criar este arquivo se quiser uma licença específica).

---

*Feito com ❤️ e muito café!*
