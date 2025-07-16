# Aprendendo Streamlit
Objetivo desse projeto é aprender algumas funções básicas de streamlit. 
Para isso foi desenvolvido uma aplicação web onde é possível fazer o upload de uma planilha
com os dados em formato .csv e o site vai ficar responsável por formatar os dados em tabela e apresentar alguns gráficos.

## Ferramentas utilizadas
- ### [Anaconda3](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
A realização do projeto foi feito dentro de um ambiente virtual a partir do anaconda. Para garantir o funcionamento na sua máquina é recomendado fazer o mesmo.

```bash
# Cria um ambiente virtual com python na versão utilizada para realização do projeto.
conda create --name streamlit-2025 python=3.13.5
```
```bash
# Ativa o ambiente virtual
conda activate streamlit-2025
```
Agora podemos instalar as bibliotecas que vamos utilizar dentro do ambiente virtual.

```bash
python -m pip install streamlit
```
- ### [Streamlit](https://docs.streamlit.io/)
Streamlit é um framework open-source do python para cientistas de dados capaz de entregar aplicativos dinâmicos de dados usando poucas linhas de código.
podemos iniciar o aplicativo com main.py utilizando o comando:
```bash 
streamlit run main.py
```
- ### Pandas
Foi utilizado para garantir a leitura dos dados e melhor estruturação das tabelas.

## Referências
Para facilitar a consulta para futuras aplicações essa área vai ficar reservada para colocar os principais métodos e comandos utilizados.

[Icones](https://streamlit-emoji-shortcodes-streamlit-app-gwckff.streamlit.app/): os icones utilizados e suportados pelo streamlit podem ser encontrados aqui.

```py
# Configurações padrões da página como título, icones, etc..
st.set_page_config(page_title=None, page_icon=None, layout=None, initial_sidebar_state=None, menu_items=None)
```

#### [file_uploader](https://docs.streamlit.io/develop/api-reference/widgets/st.file_uploader)
Exibe um widget para upload de arquivos. tendo como limite 200MB por padrão
```py
st.file_uploader(label, type=None, accept_multiple_files=False, key=None, help=None, on_change=None, args=None, kwargs=None, *, disabled=False, label_visibility="visible", width="stretch")
```

#### Comandos de exibição
```py
st.markdown() # Mostra strings em formatado como markdown.
st.dataframe() # Mostra o dataframe como uma tabela interativa.
st.expander() # Insere um container que pode ser expandido para mostrar o conteúdo ou colapsado para mostrar apenas o rótulo.
st.tabs() # Insere containers separados por janelas.
```

#### Gráficos streamlit
```py
line_chart() # Cria um gráfico interativo de linhas.
bar_chart() # Cria um gráfico interativo de barras.
```