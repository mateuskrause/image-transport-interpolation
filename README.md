# image-transport-interpolation

O processo de interpolação de imagens é definido como gerar uma imagem intermediária entre dois frames consecutivos, mantendo características de movimento e repouso.

É um processo em grande parte baseado em estimação de movimentos, que derivam diversas outras aplicações, como:
- predição de quadros e compressão de vídeo;
- aumento da taxa de quadros (*frame interpolation*);
- remoção de objetos estáticos ou compensação de movimento.

Uma das possibilidades de resolução desse problema utiliza a estimativa do [fluxo ótico](https://en.wikipedia.org/wiki/Optical_flow), onde diversos métodos e algoritmos são utilizados para analisar as diferenças entre os frames e estimar o campo de fluxo.

Porém, dado um fluxo, precisamos resolver o frame intermediário da interpolação, e para isso podemos modelar a evolução da imagem como um problema de transporte, podendo ser resolvido numericamente com diferentes técnicas.

Este repositório explora um método de resolução desse problema considerando que o fluxo é dado, focando em métodos numéricos para a resolução de equações diferenciais. A se baseia principalmente no artigo [Image sequence interpolation using optimal control](https://arxiv.org/abs/1008.0548).
