# Tetronamidas com Atividade Cianobacidal (2019)

Este conjunto de dados foi utilizado no estudo de [Acosta et al., 2019](./acosta2019.pdf), que descreve a síntese de uma nova classe de tetronamidas inspiradas em rubrolídeos, e a avaliação de sua atividade inibitória seletiva contra cianobactérias formadoras de florescimento.

## Conjunto de dados

O estudo reporta a síntese de 47 tetronamidas N-aril, abrangendo:

- **Tetronamidas intermediárias (compostos 8):** utilizadas como ponto de partida para as reações subsequentes.
- **Aldol adductos (compostos 9):** formados pela reação de tetronamidas com diversos aldeídos aromáticos.
- **Derivados 𝛾-benzylidenetetronamidas (compostos 10):** obtidos por desidratação dos adductos, quando aplicável.

## Ensaio Biológico

Os compostos foram avaliados em dois ensaios:

- **Ensaio 1 – Inibição da Cadeia de Transporte de Elétrons**: Medido pela redução da ferricianeto em cloroplastos de espinafre (reação de Hill).
- **Ensaio 2 – Inibição do Crescimento Fotoautotrófico:** Utilizando a cianobactéria *Synechococcus elongatus* como modelo.

Os valores de IC<sub>50</sub> (concentração inibitória a 50%) foram determinados para cada composto em ambos os ensaios.

## Dados

### `molecules`

Diretório com as geometrias otimizadas dos compostos. Inclui:

- `b3lyp-mol2`: geometrias otimizadas com o funcional B3LYP (`*.mol2`).
- `DFT`: outupt do Gaussian do cálculo DFT (`*.out`).

### `CEP`

Para cada composto, foram realizadas simulações de dinâmica molecular utilizando o [GROMACS](https://www.gromacs.org/). Durante as simulações, foram gerados os perfis de ensemble conformacional (CEP) a partir de frames capturados entre 50 e 500 ps. Os arquivos estão no diretório [`CEP/`](./CEP/) e contêm:

- **Topologia** (`*.top`): informações de topologia da molécula (átomos, ligações, ângulos de ligação e diedro, etc) ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#topology-file)).
- **Trajetórias** (`*.gro`): Contém as posições dos átomos da molécula em cada instante da dinâmica molecular. Se vistas como moléculas sequenciais, reproduzem a **trajetória** da dinâmica ([reference](https://manual.gromacs.org/current/reference-manual/file-formats.html#gro))
- **Perfil de Ensemble Conformacional (CEP)** (`*.pdb`): Similar ao arquivo `*.gro`, contém as posições dos átomos da molécula em cada instante da dinâmica molecular. Diferente do arquivo de trajetória (`*.gro`), este arquivo não possui informações na dimensão temporal, sendo as conformações da trajetória são sobrepostos e vistas como independentes do tempo, reproduzindo assim o CEP.
- **_Include topologies_** (`*.itp`): parâmetros de campo de força específicos para a molécula ([referência](https://manual.gromacs.org/current/reference-manual/topologies/topology-file-formats.html#molecule-itp-file)).


## Referências

Os dados presentes neste dataset foram extraídos de:

- Acosta, J. A. M., Karak, M., Barbosa, L. C. A., Boukouvalas, J., Straforini, A., & Forlani, G. (2019). *Synthesis of new tetronamides displaying inhibitory activity against bloom‐forming cyanobacteria*. Pest Management Science. DOI: [10.1002/ps.5580](https://doi.org/10.1002/ps.5580). Disponível em [`acosta2019.pdf`](./acosta2019.pdf).
