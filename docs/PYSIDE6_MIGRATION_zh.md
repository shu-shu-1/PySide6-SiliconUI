# PySide6 迁移指南

## 概述

PySide6-SiliconUI 已从 PyQt5 迁移到 PySide6。本文档提供有关更改和迁移过程的信息。

## 变更内容

### 依赖项

- **PyQt5** → **PySide6**（版本 6.0.0 或更高）
- 所有 PyQt5 导入已替换为 PySide6 等效项

### API 变更

作为迁移的一部分，进行了以下 API 更改：

| PyQt5 | PySide6 |
|-------|---------|
| `pyqtSignal` | `Signal` |
| `pyqtSlot` | `Slot` |
| `pyqtProperty` | `Property` |

### 导入变更

所有导入已更新：

```python
# 旧版 (PyQt5)
from PyQt5.QtCore import Qt, pyqtSignal
from PyQt5.QtWidgets import QWidget
from PyQt5.QtGui import QColor

# 新版 (PySide6)
from PySide6.QtCore import Qt, Signal
from PySide6.QtWidgets import QWidget
from PySide6.QtGui import QColor
```

## 安装

要使用 PySide6-SiliconUI，请使用以下命令安装：

```bash
python setup.py install
```

或手动安装依赖项：

```bash
pip install PySide6>=6.0.0 numpy pyperclip python-dateutil
```

## 兼容性

- **最低 Python 版本**：3.8
- **PySide6 版本**：6.0.0 或更高

## 用户迁移指南

如果您有使用 PyQt-SiliconUI 的现有代码，您需要：

1. 将导入从 PyQt5 更新为 PySide6
2. 将 `pyqtSignal` 替换为 `Signal`
3. 将 `pyqtSlot` 替换为 `Slot`
4. 更新依赖项以使用 PySide6 而不是 PyQt5

示例：

```python
# 旧代码
from PyQt5.QtCore import Qt, pyqtSignal
from PyQt5.QtWidgets import QApplication
import siui

class MyWidget(siui.SiWidget):
    clicked = pyqtSignal()
    
# 新代码
from PySide6.QtCore import Qt, Signal
from PySide6.QtWidgets import QApplication
import siui

class MyWidget(siui.SiWidget):
    clicked = Signal()
```

## 许可证

PySide6 在 LGPL/GPL 许可下可用，这可能与 PyQt5 的双重许可有不同的含义。请查看 [PySide6 许可文档](https://www.qt.io/licensing/) 了解详情。

## 支持

如果您在 PySide6 迁移过程中遇到任何问题，请在 [GitHub 仓库](https://github.com/shu-shu-1/PySide6-SiliconUI) 上提出问题。
