---
description: Si ce bit est défini, la barre de défilement se trouve sur le côté gauche du contrôle.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Attribut de contrôle LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99505e66f6f49b0a148b80a96d68bbef70d0f2b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515465"
---
# <a name="leftscroll-control-attribute"></a>Attribut de contrôle LeftScroll

Si ce bit est défini, la barre de défilement se trouve sur le côté gauche du contrôle.

Si ce bit n’est pas défini, la barre de défilement se trouve sur le côté droit du contrôle.

## <a name="valid-controls"></a>Contrôles valides

[ScrollableText](scrollabletext-control.md)

[VolumeCostList](volumecostlist-control.md)

[ComboBox](combobox-control.md)

[DirectoryList](directorylist-control.md)

[DirectoryCombo](directorycombo-control.md)

[Modifier](edit-control.md)

[ListBox](listbox-control.md)

[ListView](listview-control.md)

[SelectionTree](selectiontree-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                             |
|---------|-------------|--------------------------------------|
| 128     | 0x00000080  | **msidbControlAttributesLeftScroll** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit LeftScroll dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



