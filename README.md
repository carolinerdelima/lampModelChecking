# Model Checking
Modelos de sistema e verificação de propriedades sobre o modelo usando a verificador de modelos NuXMV.

Este é o README.md para o código do Trabalho 2 da disciplina de Métodos Formais para Computação, desenvolvido por Caroline Lima e Joana Figueredo.


## Como testar o código usando NuSMV
Para testar o código, usaremos a ferramenta NuSMV, que é um verificador de modelagens. Siga as etapas abaixo para executar os testes.

### Pré-requisitos
Certifique-se de ter o NuSMV instalado em seu sistema. Você pode encontrar informações sobre como baixar e instalar o NuSMV em seu site oficial: http://nusmv.fbk.eu/


### Executando os testes
1. Abra o terminal ou prompt de comando e navegue até o diretório onde o NuSMV está instalado.

2. Execute o comando abaixo para iniciar o NuSMV no modo interativo.


```
NuSMV -int
```

3. No prompt do NuSMV, execute os comandos flatten_hierarchy e encode_variables para simplificar a hierarquia do modelo e codificar as variáveis:
```
NuSMV > read_model -i lampada.smv
NuSMV > flatten_hierarchy
NuSMV > encode_variables
```
4. Construa o modelo usando o comando build_model:
```
NuSMV > build_model
```

5. Para testar as propriedades especificadas no código, você pode usar os comandos abaixo. Assim, será iniciada a execução do modelo.
``` 
pick_state
simulate -i
```
Isso iniciará a simulação interativa do modelo. Se desejar escolher estados específicos durante a simulação, você pode usar o comando pick_state -i conforme necessário.
