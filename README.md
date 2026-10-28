# Projetos de IA e automação para suporte de TI

Protótipos em Python e SQL que automatizam tarefas repetitivas de suporte, redes e monitoramento. Nasceram da minha rotina como técnico de suporte e infraestrutura e estão em evolução.

Autor: Pablo da Silva Caldeira · [LinkedIn](https://linkedin.com/in/pablo-da-silva-caldeira-5321a7321) · [Portfólio](https://pablocaldeira.github.io)

> Os trechos entre colchetes `[ ... ]` precisam ser preenchidos por você com o que o código realmente faz. Apague este aviso quando terminar.

## Projetos

| Projeto | O que resolve | Tecnologias |
| --- | --- | --- |
| [Triagem de chamados com IA](triagem-chamados-ia) | Classifica chamados e sugere a primeira resposta | Python, API de LLM |
| [Monitor de rede com alertas](monitor-rede) | Avisa quando equipamento ou câmera fica offline | Python |
| [Relatório automático de SLA](relatorio-sla) | Gera o relatório semanal de prazos sem planilha manual | SQL, Python |

---

## Triagem de chamados com IA

**Problema:** chamados chegam em texto livre e alguém precisa ler cada um para decidir o tipo e a urgência.

**O que faz:** lê o texto do chamado, classifica por tipo e prioridade e sugere a primeira resposta para o técnico revisar.

**Como funciona:**
1. Recebe o texto do chamado. [de onde: arquivo, entrada no terminal, outro]
2. Envia o texto para [nome do modelo/API de LLM usado] com um prompt de classificação.
3. Devolve o tipo, a prioridade e uma resposta sugerida.

**Como rodar:**
```bash
pip install -r requirements.txt
export [NOME_DA_VARIAVEL_DA_CHAVE]=sua_chave
python [nome_do_arquivo].py
```

**Resultado:** testei com [número] chamados de exemplo. [Quantos foram classificados corretamente / tempo da triagem manual comparado ao automático.]

**Limites:** é um protótipo. A resposta é uma sugestão e deve ser revisada por uma pessoa. [Outros limites que você conhece.]

---

## Monitor de rede com alertas

**Problema:** falhas em equipamentos e câmeras IP só eram percebidas quando alguém reclamava.

**O que faz:** testa a conexão de uma lista de equipamentos e câmeras e envia um alerta por mensagem quando algum deixa de responder.

**Como funciona:**
1. Lê a lista de dispositivos de [arquivo ou lista no código].
2. Testa cada um com [ping, requisição, outro] a cada [intervalo].
3. Envia o alerta por [Telegram, e-mail, outro] quando um dispositivo fica offline.

**Como rodar:**
```bash
pip install -r requirements.txt
python [nome_do_arquivo].py
```

**Resultado:** [quantos dispositivos monitora; se foi testado em rede real ou simulada].

**Limites:** [por exemplo, não guarda histórico de quedas].

---

## Relatório automático de SLA

**Problema:** o relatório semanal de prazos dependia de uma planilha montada à mão.

**O que faz:** consulta os chamados no banco de dados, calcula quantos foram atendidos dentro do prazo e gera o relatório da semana.

**Como funciona:**
1. Executa uma consulta SQL em [banco usado: SQLite, MySQL, outro].
2. Calcula os prazos cumpridos em Python.
3. Gera o relatório em [CSV, Excel, PDF, texto].

**Como rodar:**
```bash
pip install -r requirements.txt
python [nome_do_arquivo].py
```

**Resultado:** [tempo que a montagem manual levava comparado ao automático; se usou dados reais ou de exemplo].

**Limites:** [por exemplo, os dados do banco são de exemplo].

---

## Próximos passos

- [Algo que você pretende melhorar, por exemplo: rodar a triagem com n8n, publicar uma demo, criar um painel para o relatório de SLA.]
