---
description: Si ce bit de style est défini, le texte du contrôle est affiché dans un ordre de lecture de droite à gauche.
ms.assetid: 68394498-98ca-4bcd-86c0-3f692a26a258
title: Attribut de contrôle RTLRO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c452a4b5b4533b24e8e59b6fe70dc2884baec0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518828"
---
# <a name="rtlro-control-attribute"></a>Attribut de contrôle RTLRO

Si ce bit de style est défini, le texte du contrôle est affiché dans un ordre de lecture de droite à gauche.

## <a name="valid-controls"></a>Contrôles valides

[GroupBox](groupbox-control.md)

 

[Barre de progression](progressbar-control.md)

 

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



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit RTLRO dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



