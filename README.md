# Weppy Tutorial

[Weppy](http://weppy.org) é um framework full-stack escrito em Python desenhado com simplicidade em mente.

Este tutorial é baseado no tutorial original [http://weppy.org/docs/1.1/tutorial](http://weppy.org/docs/1.1/tutorial).

## Como rodar a aplicação

```
git clone https://github.com/rg3915/weppy-tutorial.git
cd weppy-tutorial
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Rodando o Hello World

```
python hello.py
```

A aplicação roda local na porta 8000.

### Rodando o Bloggy

Primeiro faça a migração do banco

```
cd bloggy
weppy -a bloggy.py migrations generate -m "First migration"
weppy -a bloggy.py migrations up
weppy --app bloggy.py setup
```

Rode a aplicação a partir da pasta `bloggy`.

```
weppy --app bloggy.py run
```

