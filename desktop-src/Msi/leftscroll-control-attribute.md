---
description: Si ce bit est défini, la barre de défilement se trouve sur le côté gauche du contrôle.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Attribut de contrôle LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3bfbfd0ce92e337b7de3504847c39a3b2250562f05f18280a8f46916909fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043249"
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



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit LeftScroll dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



