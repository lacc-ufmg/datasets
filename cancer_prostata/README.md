# Inibidores da 17β-HSD3 - Tratamento de Câncer de Próstata (2012)

Este dataset foi utilizado no estudo 4D-QSAR receptor independente para inibidores da enzima 17β-hidroxiesteroide desidrogenase tipo 3 (17β-HSD3), um alvo relevante no tratamento do câncer de próstata. A 17β-HSD3 é responsável pela conversão de androstenediona em testosterona, e sua inibição pode reduzir os níveis de androgênios, hormônios essenciais para o crescimento prostático.


## Descrição do conjunto

Este conjunto é composto por 49 derivados de benzilideno oxazolidindiona e tiazolidindiona. Estes compostos foram sintetizados e reportados por Harada et al. e avaliados quanto à sua atividade inibitória contra 17β-HSD3. Os ensaios *in vitro* utilizaram células HeLa transfectadas com 17β-HSD3. A atividade foi medida em termos de IC50 (concentração inibitória, em nM) e, para melhor distribuição dos dados, os valores foram convertidos para pIC50 (–log IC50).

## Dados

Os compostos foram construídos a partir de um arquivo de geometria obtido do banco de dados ZINC. As estruturas foram otimizadas utilizando o software HyperChem e submetidas a cálculos em diferentes níveis de teoria (MM+, AM1, Hartree–Fock e DFT). Para cada composto, foram realizadas simulações de dinâmica molecular utilizando o [GROMACS](https://www.gromacs.org/). Durante as simulações, foram gerados os perfis de ensemble conformacional (CEP) a partir de frames capturados entre 50 e 500 ps.

- **Topologia** (`*.top`): informações de topologia da molécula (átomos, ligações, ângulos de ligação e diedro, etc) ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#topology-file)).
- **Trajetórias** (`*.gro`): perfil de amostragem conformacional (_conformational enseble profile_ ou CEP). Contém as posições dos átomos da molécula em cada instante da dinâmica molecular. Se vistas como moléculas sequenciais, reproduzem a **trajetória** da dinâmica; se sobrepostos e vistos como independentes do tempo, reproduzem o CEP. ([reference](https://manual.gromacs.org/current/reference-manual/file-formats.html#gro))
- **_Include topologies_** (`*.itp`): parâmetros de campo de força específicos para a molécula ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#molecule-itp-file)).


As atividades biológicas experimentais estão no arquivo `atividades.csv`, que contém o nome e pIC50 de cada composto.


## Referências

Os dados presentes neste dataset foram extraídos de:

- Martins, J. P. A. & de Melo, E. B. (2019). *4D-QSAR Study of 17β-Hydroxysteroid Dehydrogenase Type 3 Inhibitors*. J. Braz. Chem. Soc., 30(7), 1548–1557.
- Harada,  K.;  Kubo,  H.; Abe,  J.;  Haneta,  M.;  Conception, A.;  Inoue, S.; Okada, S.; Nishioka, K.; Bioorg. Med. Chem. 2012, 20, 3242.
