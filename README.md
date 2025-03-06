
# LexFlow - Automação de Contratos Jurídicos

Projeto que automatiza a geração de contratos jurídicos em massa, utilizando Python, Jupyter Notebook e pandas para manipular dados, além de templates no Microsoft Word via biblioteca python-docx. Criado para demonstrar habilidades em integrar tecnologia e direito, destacando práticas ágeis (Agile/Scrum).


##  Tecnologias
Python 3.x

Jupyter Notebook

pandas

python-docx

## Pré-requisitos

Python 3.x instalado

Jupyter Notebook (ou JupyterLab)

Git (para versionamento e colaboração)

Microsoft Word (ou editor compatível para abrir e editar .docx)
## Instalação

1. Clone o repositório:
git clone 
https://github.com/seuusuario/lexflow-automacao-contratos.git

2. Entre no diretório do projeto:
cd lexflow-automacao-contratos

3. Instale as dependências:
pip install -r requirements.txt

## Uso
1. Abra o Jupyter Notebook:
jupyter notebook

2. Navegue até o arquivo principal (por exemplo, lexflow.ipynb) e execute as células em sequência.

3. Personalize as variáveis de acordo com suas necessidades (nomes, datas, itens etc.).

4. Gere os contratos. Exemplo de trecho de código:
from docx import Document
from datetime import datetime
import pandas as pd

documento = Document("ContratoTemplate.docx")
# Ajuste o dicionário de referências
referencias = {
    "NOME": "Lira",
    "ITEM1": "Carro",
    "ITEM2": "Notebook",
    "ITEM3": "Celular",
    "DD": str(datetime.now().day),
    "MM": str(datetime.now().month).zfill(2),
    "AAAA": str(datetime.now().year),
}

for paragrafo in documento.paragraphs:
    for codigo, valor in referencias.items():
        paragrafo.text = paragrafo.text.replace(codigo, valor)

documento.save("Contrato-Gerado.docx")


## Licença
Distribuído sob licença MIT. Consulte o arquivo LICENSE para detalhes.

Uso comercial: Permitido, seguindo os termos da licença.
Educacional: Livre para estudos e inspirações.
## Badges
Manutenção ativa:

Licença:

Python 3.x:

pandas:

Jupyter Notebook:


PRs Welcome:
## Contribuição
Faça um fork do repositório.

Crie uma branch com sua feature ou correção.

Abra um Pull Request descrevendo suas alterações.
## Contribuidor
Pedro Henrique - https://github.com/PedroHenrique-creator/LexFlow