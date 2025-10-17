# PySide6 Migration Guide

## Overview

PySide6-SiliconUI has been migrated from PyQt5 to PySide6. This document provides information about the changes and migration process.

## What Changed

### Dependencies

- **PyQt5** → **PySide6** (version 6.0.0 or higher)
- All PyQt5 imports have been replaced with PySide6 equivalents

### API Changes

The following API changes were made as part of the migration:

| PyQt5 | PySide6 |
|-------|---------|
| `pyqtSignal` | `Signal` |
| `pyqtSlot` | `Slot` |
| `pyqtProperty` | `Property` |

### Import Changes

All imports have been updated:

```python
# Old (PyQt5)
from PyQt5.QtCore import Qt, pyqtSignal
from PyQt5.QtWidgets import QWidget
from PyQt5.QtGui import QColor

# New (PySide6)
from PySide6.QtCore import Qt, Signal
from PySide6.QtWidgets import QWidget
from PySide6.QtGui import QColor
```

## Installation

To use PySide6-SiliconUI, install it with:

```bash
python setup.py install
```

Or install the dependencies manually:

```bash
pip install PySide6>=6.0.0 numpy pyperclip python-dateutil
```

## Compatibility

- **Minimum Python Version**: 3.8
- **PySide6 Version**: 6.0.0 or higher

## Migration for Users

If you have existing code using PyQt-SiliconUI, you need to:

1. Update your imports from PyQt5 to PySide6
2. Replace `pyqtSignal` with `Signal`
3. Replace `pyqtSlot` with `Slot`
4. Update your dependencies to use PySide6 instead of PyQt5

Example:

```python
# Old code
from PyQt5.QtCore import Qt, pyqtSignal
from PyQt5.QtWidgets import QApplication
import siui

class MyWidget(siui.SiWidget):
    clicked = pyqtSignal()
    
# New code
from PySide6.QtCore import Qt, Signal
from PySide6.QtWidgets import QApplication
import siui

class MyWidget(siui.SiWidget):
    clicked = Signal()
```

## License

PySide6 is available under LGPL/GPL licensing, which may have different implications than PyQt5's dual licensing. Please review the [PySide6 licensing documentation](https://www.qt.io/licensing/) for details.

## Support

If you encounter any issues with the PySide6 migration, please open an issue on the [GitHub repository](https://github.com/shu-shu-1/PySide6-SiliconUI).
