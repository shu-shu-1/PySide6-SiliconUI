
<p align="center">  
  
  <a href="#">
    <img src="https://github.com/ChinaIceF/PySide6-SiliconUI/blob/main/assets/readme/silicon_main.png?raw=true" alt="Logo"  >
  </a>
  
  <h2 align="center">PySide6-SiliconUI</h2>
  <p align="center">A powerful and artistic UI library based on PySide6</p>

<p align="center">
    English | <a href="docs/README_zh.md">简体中文</a>
</p>

## Install
Clone this repository and run the following command in your terminal:

```cmd
python setup.py install
```

Or install dependencies with pip:

```cmd
pip install PySide6>=6.0.0 numpy pyperclip python-dateutil
```

> ⚠️ This project is still under active development. It is **not yet available on PyPi**, but will be in the future.

## PySide6 Migration

This library has been migrated from PyQt5 to PySide6. For migration details and compatibility information, see the [PySide6 Migration Guide](docs/PYSIDE6_MIGRATION.md).


## Run the Example Gallery
To explore the widgets, components, and framework offered by PySide6-SiliconUI, run 
```
examples/Gallery for siui/start.py
```

### Refactoring Plan

The refactoring of widgets is nearing completion. You can try them on the "Refactored Widgets" page in the Gallery.

**Please note**:  
If you plan to start a project using PySide6-SiliconUI in the near future, it is **highly recommended to use only the widgets listed under “Refactored Widgets”**. 
The older widgets have many issues and are being gradually replaced.  

Similarly, the application templates are also under a complete overhaul. Work on them will begin once the core widget and component refactors are done. 
Since the current templates contain many flaws and have poor implementations, 
**we strongly advise against using the old application templates for real-world projects until the refactor is complete**.

### Refactored Modules Overview

Below are actively maintained modules. Once these are fully implemented, outdated ones will be removed from the repository.

#### Widgets

- `siui/components/button.py` – Refactored button widgets  
- `siui/components/container.py` – Refactored containers managed using Qt’s layout system  
- `siui/components/editor.py` – Refactored input/edit widgets  
- `siui/components/graphic.py` – Proxy widgets, wrappers, and graphic-related utilities  
- `siui/components/label.py` – Widgets for displaying text and images, plus uncategorized ones  
- `siui/components/layout.py` – New implementations of flow and waterfall layouts, also using Qt layouts  
- `siui/components/menu_.py` – Menu components  
- `siui/components/popover.py` – Popover-style widgets such as date pickers and time pickers  
- `siui/components/progress_bar_.py` – Refactored progress bar widgets  
- `siui/components/slider_.py` – Refactored sliders, including horizontal sliders and scrollbar handles  

#### Core Features

- `siui/core/animation.py` – Refactored animation utilities  
- `siui/core/event_filter.py` – Various event filters  
- `siui/core/painter.py` – Core drawing-related functions  


## See Also
Here are some project that created based on PySide6-SiliconUI:
* [My-TODOs](https://github.com/ChinaIceF/My-TODOs) - A cross-platform desktop To-Do list.


## License
PySide6-SiliconUI is licensed under [GPLv3](LICENSE) 

Copyright © 2024-2025 by ChinaIceF.