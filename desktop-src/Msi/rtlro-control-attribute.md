---
description: Si ce bit de style est défini, le texte du contrôle est affiché dans un ordre de lecture de droite à gauche.
ms.assetid: 68394498-98ca-4bcd-86c0-3f692a26a258
title: Attribut de contrôle RTLRO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c4488b31b0bac714d0f28915c074c0a6e4a8b5105e3ef2be60f3870ebcf88d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039669"
---
# <a name="rtlro-control-attribute"></a>Attribut de contrôle RTLRO

Si ce bit de style est défini, le texte du contrôle est affiché dans un ordre de lecture de droite à gauche.

## <a name="valid-controls"></a>Contrôles valides

[GroupBox](groupbox-control.md)

 

[ProgressBar](progressbar-control.md)

 

[Boutons](pushbutton-control.md)

 

[ScrollableText](scrollabletext-control.md)

 

[Text](text-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[CheckBox](checkbox-control.md)

 

[ComboBox](combobox-control.md)

 

[DirectoryList](directorylist-control.md)

 

[DirectoryCombo](directorycombo-control.md)

 

[Modifier](edit-control.md)

 

[PathEdit](pathedit-control.md)

 

[ListBox](listbox-control.md)

 

[ListView](listview-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

 

[SelectionTree](selectiontree-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                        |
|---------|-------------|---------------------------------|
| 32      | 0x00000020  | **msidbControlAttributesRTLRO** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit RTLRO dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



