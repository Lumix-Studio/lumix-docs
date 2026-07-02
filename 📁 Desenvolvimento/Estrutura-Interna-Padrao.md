

## 📂 Padrão de Estrutura Interna Dos Jogos em Godot


```
res://
├── docs/
│   └── developer_doc/
├── assets/
│   ├── models # assets 3D
│   ├── themes
│   └── ui
├── src/
│   ├── autoloads
│   ├── config
|   ├── objects
│   ├── entities/
│   │   ├── player/
│   │   │   ├── assets/
│   │   │   │   ├── sprites
│   │   │   │   ├── audio
│   │   │   │   └── materials
│   │   │   ├── player.tscn
│   │   │   └── player.gd
│   │   └── enemies/
│   │       └── enemy_type_0/
│   │           ├── assets/
│   │           │   ├── sprites
│   │           │   ├── audio
│   │           │   └── materials
│   │           ├── enemy_type_0.tscn
│   │           └── enemy_type_0.gd
│   ├── maps/
│   ├── systems/
│   └── ui/
├── .editorconfig
├── .gitignore
├── icon.png
├── project.godot
└── README.md
```
### 📘 Definições:
| Pasta   | Caminho                | Objetivo                                                                                       |
| ------- | ---------------------- | ---------------------------------------------------------------------------------------------- |
|docs     |`res://docs/`           | Centraliza toda e qualquer tipo de documentação do projeto                                     |
|assets   |`res://assets/`         | Centraliza todos assets **exceto sprites ou modelos de personagems ou mapas**                  |
|src      |`res://src/`            | Centraliza todo código fonte, mecânicas e funcionalidade do jogo                               | 
|autoloads|`res://src/autoloads`   | Guarda todos os singletons do jogo                                                             |
|config   |`res://src/config`      | Guarda arquivos de dados estaticos (Resources, JSONs...) e template de resource                |
|objects  |`res://src/objects`     | Guarda códigos e Cenas de objeto de mapa com sistema proprio. ex: TV                           |
|entities |`res://src/entities`    | Guarda códigos e Cenas de personagens (player, inimigos, bosses e NPC...)                      |
|maps     |`res://src/maps`        | Guarda códigos e Cenas dos mapas de todo o jogo                                                |
|systems  |`res://src/systems`     | Guarda códigos de lógica global do jogo, sem precisarem ser autoloads, ex: CombatSystem        |
|ui       |`res://src/ui`          | Guarda códigos e Cenas de interface grafica                                                    |

> Repare que em **entities** cada subpasta coresponde a um **personagem**.
> E cada personagem contém uma pasta de assets própria Ex: **res://src/entities/player/assets**  Isso evita centralizar tudo na pasta de assets gerais **res://assets** 
---
### 📒 Pasta Docs/developer_doc

```
docs/
└── developer_doc/
    ├── save_manager.txt # ou .md
    ├── physic_system.txt
    ├── game_system.txt
    └── ...
```

Como mais de um desenvolvedor pode ocasionalmente mexer no código do outro. Cada sistema deve conter um arquivo .md explicando seu funcionamento e como integrar com o restante do projeto, no início de cada documentação.
É recomendado ter o nome do desenvolvedor que desenvolveu o código.