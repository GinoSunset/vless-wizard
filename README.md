# Vless Wizard

**Vless Wizard** — это  мастер настройки **3x-ui** панелей через SSH.
Он автоматически подключается к серверу, при необходимости устанавливает 3x-ui.

Инструкции по работе с ним можно найти на [этой странице](https://github.com/YukiKras/vless-wizard/wiki)

## Windows

Самый простой способ — использовать готовый установщик.

📦 **Скачать последнюю версию:**
👉 [Vless Wizard установщик для Windows](https://github.com/YukiKras/vless-wizard/releases/latest/download/VlessWizard_Setup.exe)

После установки запустите **Vless Wizard** из меню «Пуск» или с рабочего стола.

## Linux / macOS

### 1. Установите зависимости

Убедитесь, что у вас установлен **Python 3.10+**.
Затем выполните команды:

```bash
git clone https://github.com/YukiKras/vless-wizard.git
cd vless-wizard
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

> Если вы видите ошибку `pip: command not found`, установите пакетный менеджер Python:
> ```bash
> sudo apt install python3-pip  # Ubuntu/Debian
> brew install python3          # macOS (через Homebrew)
> ```

### 2. Запустите мастер

```bash
python main.py
```

Приложение запустится в оконном режиме.

## Сборка установщика (для разработчиков Windows)

Если вы хотите собрать `.exe` самостоятельно:

```bash
pip install pyinstaller
pyinstaller --noconfirm --onedir --windowed --add-data "3xinstall.sh;." main.py
```

Готовый установщик появится в папке `dist/`.
