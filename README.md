# ST_Intersects

Explicação do Código:
gpd.sjoin: Esta função é do módulo geopandas e realiza um spatial join (junção espacial) entre dois GeoDataFrames.

gdf_escolas_sp: Este é o primeiro GeoDataFrame que contém as geometrias das escolas. Ele será combinado com o segundo GeoDataFrame.

gdf_sp: Este é o segundo GeoDataFrame, que contém as geometrias dos municípios.

how='inner': Esse parâmetro determina o tipo de junção. Com 'inner', apenas as linhas que têm correspondência em ambos os GeoDataFrames (ou seja, onde as geometrias se sobrepõem) serão incluídas no resultado. Em outras palavras, ele retorna apenas os dados que têm uma relação espacial.

predicate='intersects': Este parâmetro especifica a condição espacial que deve ser satisfeita para que as linhas sejam combinadas. intersects significa que o código vai incluir apenas as escolas que intersectam (ou se sobrepõem) com os municípios. Se uma escola estiver localizada dentro dos limites de um município, ela será incluída na saída.

Resultado:
O resultado dessa operação será um novo GeoDataFrame chamado gdf_intersects, que contém apenas as escolas que estão dentro ou tocam os limites dos municípios, juntamente com as informações de ambos os conjuntos de dados. Isso é útil para análises que envolvem a relação espacial entre diferentes entidades geográficas, como a distribuição de escolas em relação aos municípios.
