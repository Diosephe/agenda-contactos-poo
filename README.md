# agenda-contactos-poo

## Qué hace el sistema (1–2 líneas)
Sistema de gestión de contactos en Python (POO) que permite registrar, buscar, editar y eliminar contactos usando encapsulación y estructuras de datos (listas y diccionarios).

## Funcionalidades (bullets)
- Agregar contacto (nombre, teléfono, correo, dirección)
- Listar contactos
- Buscar por nombre (coincidencia parcial / substring)
- Buscar por teléfono
- Editar contacto
- Eliminar contacto
- Validaciones básicas de teléfono y correo
- Pruebas unitarias con `unittest`

## Estructura del repo (mini árbol)
agenda-contactos-poo/
├─ agenda_contactos.py
├─ README.md
└─ docs/
   ├─ evidencia_tests.txt
   └─ demo.md

## Módulos utilizados
- Python 3 (sin librerías externas)
- `unittest` (librería estándar de Python) para pruebas unitarias

## Arquitectura (resumen)
- `Contacto`: modela un contacto individual y aplica encapsulación con atributos internos y `@property` (validaciones en setters).
- `AgendaContactos`: gestiona el conjunto de contactos y operaciones CRUD (agregar, listar, buscar, editar, eliminar) usando:
  - una LISTA para mantener y listar contactos,
  - DICCIONARIOS para acceso/búsqueda rápida y control de duplicados (por ejemplo, por teléfono).
- `ejecutar_menu()`: prototipo funcional para operar la agenda desde consola.

## Cómo ejecutar el menú (Colab y/o local)

### En Google Colab
1) Abre un notebook en Google Colab.
2) Sube `agenda_contactos.py` al notebook (o copia/pega el código).
3) En una celda ejecuta:
   from agenda_contactos import ejecutar_menu
   ejecutar_menu()

### En entorno local (PC)
Requisito: tener Python 3 instalado.
1) Descarga o clona el repositorio y entra a la carpeta del proyecto.
2) Abre una terminal (CMD/PowerShell/Terminal).
3) Ejecuta el archivo con:
   python agenda_contactos.py
4) Se mostrará un menú en consola para agregar, listar, buscar, editar y eliminar contactos.

## Cómo correr tests (Colab y/o local)

### En Google Colab / Jupyter
Con `agenda_contactos.py` cargado, en una celda ejecuta:
import unittest
_ = unittest.main(argv=[''], exit=False)

### En entorno local (PC)
En la carpeta del proyecto ejecuta:
python -m unittest agenda_contactos -v
Si todo está correcto, el resultado final mostrará OK.

## Evidencia
- Resultado de tests: docs/evidencia_tests.txt
- Checklist / link de demo: docs/demo.md
