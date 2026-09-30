# Lesson 3 — решения (Jupyter notebook)

Ноутбук с решениями задач занятия 3.

## Содержимое

| Файл | Описание |
| --- | --- |
| `lesson_3.ipynb` | ЗАДАЧА 1 (ABBREVIATION), ЗАДАЧА 2 (CALCULATOR) |
| `requirements.txt` | зависимости для запуска ноутбука |

Сторонние библиотеки не используются — только стандартная библиотека Python,
поэтому достаточно установить Python 3.10+ и Jupyter.

## Как запустить на другой машине

### 1. Клонировать репозиторий

```bash
git clone https://github.com/DS-BY/IT-Academy-PY.git
cd IT-Academy-PY
```

### 2. Создать окружение и установить зависимости

macOS / Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Windows (PowerShell):

```powershell
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Вариант через conda:

```bash
conda create -n it-academy python=3.10 -y
conda activate it-academy
pip install -r requirements.txt
```

### 3. Открыть ноутбук

```bash
jupyter notebook lesson_3.ipynb
# или
jupyter lab lesson_3.ipynb
```

### 4. VS Code

1. Открыть папку с проектом (`File → Open Folder`).
2. Установить расширение **Jupyter** (Microsoft).
3. `Select Kernel...` → выбрать созданное окружение (`.venv` или `it-academy`).
4. `Run All` / выполнять ячейки по одной.

### 5. Google Colab (если Python не хочется ставить локально)

* <https://colab.research.google.com> → `File → Upload notebook` → выбрать `lesson_3.ipynb`, либо
* `File → Open notebook → GitHub` → вставить `https://github.com/DS-BY/IT-Academy-PY`.

## Важно про `input()`

Каждая задача читает данные через `input(...)`, поэтому ячейки нужно запускать
**интерактивно** (в Jupyter/VS Code/Colab ввод появится под ячейкой).
Автоматический прогон `jupyter nbconvert --execute` без поданного stdin зависнет
на ожидании ввода.

## Как сохранить изменения обратно в GitHub

```bash
git add -A
git commit -m "Описание изменений"
git push
```

Перед коммитом можно очистить сохранённые выводы ячеек (чтобы в репозиторий
не попадали случайные результаты запусков):

```bash
jupyter nbconvert --clear-output --inplace lesson_3.ipynb
```
