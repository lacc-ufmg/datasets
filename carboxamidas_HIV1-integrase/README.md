# Carboxamidas Inibidoras de HIV-1 Integrase

Este *dataset* contém um conjunto de 33 carboxamidas derivadas da 4,5-dihidroxypirimidina, potenciais inibidoras do HIV-1 integrase. Os dados foram extraídos de pesquisas publicadas que investigam a atividade biológica e as propriedades estruturais desses compostos.

## Dados

Os dados foram obtidos a partir da dinâmica molecular com o [GROMACS](https://www.gromacs.org/) + [topolbuild](https://ftp.gromacs.org/contrib/tools/), estando disponíveis no diretório `gromacs/` os seguintes arquivos para cada molécula:

- **Topologia** (`*.top`): informações de topologia da molécula (átomos, ligações, ângulos de ligação e diedro, etc) ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#topology-file)).
- **Trajetórias** (`*.gro`): perfil de amostragem conformacional (_conformational enseble profile_ ou CEP). Contém as posições dos átomos da molécula em cada instante da dinâmica molecular. Se vistas como moléculas sequenciais, reproduzem a **trajetória** da dinâmica; se sobrepostos e vistos como independentes do tempo, reproduzem o CEP. ([reference](https://manual.gromacs.org/current/reference-manual/file-formats.html#gro))
- **_Include topologies_** (`*.itp`): parâmetros de campo de força específicos para a molécula ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#molecule-itp-file)).

Além disso, também está disponível um conjunto para validação externa.

As atividades biológicas experimentais estão no arquivo `atividades.csv`, que contém o nome e pIC50 de cada composto.

## Referências

Os dados presentes neste dataset foram extraídos de dois artigos:

- MARTINS et al. *Web-4D-QSAR: A Web-Based Application to Generate 4D-QSAR Descriptors*. Journal of Computational Chemistry, 2018. Disponível em [`ataidemartins2018.pdf`](./ataidemartins2018.pdf).
- PETROCCHI et al. *From dihydroxypyrimidine carboxylic acids to carboxamide HIV-1 integrase inhibitors: SAR around the amide moiety*. 2007. Disponível em [`petrocchi2007.pdf`](./petrocchi2007.pdf).
