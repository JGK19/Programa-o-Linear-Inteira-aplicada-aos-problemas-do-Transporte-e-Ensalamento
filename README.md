## Programa de Programação Linear Inteira aplicada aos Problemas do Transporte e Ensalamento

Este repositório reúne algoritmos e ferramentas para resolver e analisar problemas de transporte e ensalamento, utilizando métodos exatos (programação linear inteira) e heurísticas. O projeto permite gerar instâncias, aplicar diferentes métodos de solução, comparar desempenho e visualizar resultados.

### Instalação
1. Certifique-se de ter o Python instalado.
2. Instale as dependências:
	 ```bash
	 pip install -r requirements.txt
	 ```

### Estrutura dos scripts de solução
Os principais scripts aceitam argumentos para customizar a execução. Exemplos:

#### Ensalamento
- Gerar instâncias:
	```bash
	python src/ensalamento/gerador.py
	```
	(sem argumentos via linha de comando)
- Heurística gulosa:
	```bash
	python src/ensalamento/guloso.py -i 1001 -j 1001 --min_alunos 10 --max_alunos 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instancias
	```
- Método húngaro:
	```bash
	python src/ensalamento/hungaro.py -i 1001 -j 1001 --min_alunos 10 --max_alunos 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instancias
	```
- Método AMPL:
	```bash
	python src/ensalamento/ensalamento_ampl.py -i 1001 -j 1001 --min_alunos 10 --max_alunos 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instancias --solver highs
	```

#### Transporte
- Gerar instâncias:
	```bash
	python src/transporte/gerador.py --num_origens 10 --num_destinos 20 --seed 42
	```
- Método clássico:
	```bash
	python src/transporte/tClassico.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- Método canto noroeste:
	```bash
	python src/transporte/tCantoNoroeste.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- Método Vogel:
	```bash
	python src/transporte/tVogel.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- Método AMPL:
	```bash
	python src/transporte/tClassico_ampl.py 1001 1001 --min_val 1 --max_val 100 --seed 42 --solver highs
	```
- Heurísticas:
	```bash
	python src/transporte/tGenetico.py 1001 1001 --min_val 1 --max_val 100 --seed 42 --geracoes 100 --populacao 100
	python src/transporte/tGuloso.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	python src/transporte/tRestrito.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```

Consulte os comentários nos scripts para detalhes sobre cada abordagem e argumentos opcionais.

---

## Integer Linear Programming applied to Transportation and Classroom Assignment Problems

This repository gathers algorithms and tools to solve and analyze transportation and classroom assignment problems using exact methods (integer linear programming) and heuristics. The project allows instance generation, applying different solution methods, performance comparison, and result visualization.

### Installation
1. Make sure you have Python installed.
2. Install dependencies:
	 ```bash
	 pip install -r requirements.txt
	 ```

### Solution scripts structure
Main scripts accept arguments to customize execution. Examples:

#### Classroom Assignment
- Generate instances:
	```bash
	python src/ensalamento/gerador.py
	```
	(no command-line arguments)
- Greedy heuristic:
	```bash
	python src/ensalamento/guloso.py -i 1001 -j 1001 --min_students 10 --max_students 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instances
	```
- Hungarian method:
	```bash
	python src/ensalamento/hungaro.py -i 1001 -j 1001 --min_students 10 --max_students 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instances
	```
- AMPL method:
	```bash
	python src/ensalamento/ensalamento_ampl.py -i 1001 -j 1001 --min_students 10 --max_students 90 --min_cap 30 --max_cap 90 --min_d 1 --max_d 10 --seed 42 --folder instances --solver highs
	```

#### Transportation
- Generate instances:
	```bash
	python src/transporte/gerador.py --num_sources 10 --num_destinations 20 --seed 42
	```
- Classic method:
	```bash
	python src/transporte/tClassico.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- Northwest corner method:
	```bash
	python src/transporte/tCantoNoroeste.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- Vogel method:
	```bash
	python src/transporte/tVogel.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```
- AMPL method:
	```bash
	python src/transporte/tClassico_ampl.py 1001 1001 --min_val 1 --max_val 100 --seed 42 --solver highs
	```
- Heuristics:
	```bash
	python src/transporte/tGenetico.py 1001 1001 --min_val 1 --max_val 100 --seed 42 --generations 100 --population 100
	python src/transporte/tGuloso.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	python src/transporte/tRestrito.py 1001 1001 --min_val 1 --max_val 100 --seed 42
	```

Check script comments for details about each approach and optional arguments.
