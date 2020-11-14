lista = ['oi#', '%abcde', 'rolo doido', 'remove isso', '', 1, 2.343424]

#remover caracter q n quero na lista
#convertendo tudo pra str

nova_lista = [i.strip('escrever oq quer remover aqui') if type(i)== str else str(i) for i in budget]

nova_lista = [i.strip('# % remove isso ') if type(i)== str else str(i) for i in budget]

print(nova_lista)
['oi', 'abcde', 'rolo doido', '', '', '1', '2.343424']

#remover whitespace

no_whitespace = [i for i in nova_lista if i.strip()]

print(no_whitespace)
['oi', 'abcde', 'rolo doido', '1', '2.343424']


**Filtrando colunas a partir de uma determinada string** 

* Usa-se o metodo str.contains('nome q deseja filtrar')
* ele retorna a string desejada em qualquer posicao
* o argumento case=False é tirar o case sensitive


usa_and_others = movies_data[movies_data['country'].str.contains('USA',case=False)==True]


usa_and_others.head()

**atualizando colunas com valores errados**

#seleciona as linhas com idade negativa

dataframe.loc[base['age']<0]

#pega somente a media das idades positivas

dataframe.loc[base['age']>0].mean()

#atribui às idades negativas a media das idades

dataframe.loc[base['age']<0,'age'] = 40

**preenchendo NaN values**

df.fillna(df.loc[column != 'NaN', 'column'].mean(), inplace=True)

**Preenchendo colunas NaN com determinado valor usando dic**


#categorical value

df = df.fillna({"Column": "Value"})

#another method

values = {'Column1': Value1, 'Column2': Value2, 'Column3': Value3, 'Column4': Value4}
df.fillna(value=values)
