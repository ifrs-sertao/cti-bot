<!-- <!-- ---
marp: true
theme: uncover
_class: invert -->


# Estudos Rasa e Rasa X

Rasa é um framework open source  de desenvolvimento de assitentes virtuais (chatbot) com Inteligência Artifical

---

# Rasa X 
É um assistente para Conversation-Driven Development (CDD)

O processo de ouvir seus usuários e usar esses insights para melhorar seu assistente de IA.


# Fluxo E-mail Institucional

Nesse fluxo é interessante abordar desde os passos e requisitos básicos para ativar o e-mail até resolução de problemas de acesso.

## Desafio de Intents vs Entities
Como os fluxos de primeiro ao email e de resolução de problemas podem ser ambiguos, talvez aqui seja necessário estudar melhor sobre a criaçãod e Entidades (_Entities_) ao invés de segmentar tudo em Intenções (_Intents_) 

Exemplo de _Intent_ criada para o fluxo que representa um passo a passo ( manual ) de acesso ao e-mail:

```yml
- intent: acessoemail_manual
  examples: |
    - Como acesso o e-mail institucional
    - Como faço para acessar o e-mail institucional
    - Não sei como acessa o e-mail institucional
    - Não consigo acessar o e-mail institucional
    - Preciso acessar meu email
    - Preciso acessar meu email institucional
    - Como entro no email institucional
    - Como entro no email
    - Como acesso meu gmail institucional

```

Aqui um fluxo para entender uma _intent_ relacionada a problemas de acesso ao email institucional:

```yml
- intent: acessoemail_problema
  examples: |
    - Meu e-mail institucional não entra
    - Meu e-mail institucional dá erro
    - Meu e-mail institucional diz que não existe
    - O e-mail institucional diz que usuário ou senha estão errados
```

Na documentação do Rasa há um tópico sobre [Melhores Práticas em Reconhecimento de Linguagem Natural - NLU ](https://rasa.com/docs/rasa/generating-nlu-dat) que trata da Confusão de Intenções e como usar Entidades para mitigar isso.