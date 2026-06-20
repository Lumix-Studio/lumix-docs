

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
│   ├── entities/          # exemplo dos personagens
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