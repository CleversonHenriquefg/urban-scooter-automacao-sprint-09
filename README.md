# Automação da Tarefa 1 — Urban Scooter

Testes Selenium para os campos Nome, Sobrenome e Telefone da primeira etapa de “Fazer pedido”.

## Preparação no PyCharm

1. Crie uma pasta chamada `urban_scooter_automation`.
2. Copie para ela os quatro arquivos deste projeto.
3. Crie/ative o ambiente virtual do PyCharm.
4. No terminal do PyCharm, execute:

```bash
python -m pip install -r requirements.txt
python -m pytest -v
```

O Selenium abre o Chrome em 1280x720, executa os 20 cenários e fecha o navegador ao final.

## Observação sobre Opera

O projeto automatiza a execução no Chrome. Para a exigência da TripleTen, execute também os mesmos 20 cenários manualmente no Opera 71 ou superior, também em 1280x720, e preencha as colunas correspondentes na planilha.

## Estrutura

- `data.py`: URL e dados válidos de apoio.
- `pages.py`: Page Object Model e localizadores.
- `test_urban_scooter.py`: casos de teste parametrizados.
- `requirements.txt`: bibliotecas necessárias.
- `conftest.py`: captura de evidências quando um teste falha.

## Evidências de falha

Se algum caso falhar, o Pytest salva automaticamente dois arquivos na pasta
`evidencias/`:

- um print da tela em `.png`;
- um relatório em `.txt` com o teste, URL, horário e a mensagem da falha.

Esses arquivos servem como evidência para criar o bug no Jira. Um teste
negativo que passa não é bug: ele apenas confirma que a validação funcionou.
