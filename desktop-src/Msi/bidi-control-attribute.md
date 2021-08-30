---
description: Il s’agit d’une combinaison de l’ordre de lecture de droite à gauche RTLRO, RightAligned et LeftScroll attributs.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Attribut de contrôle BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5fd152bbff384961a51350d31759b35ea2b0b4444cac20c78df3dbc7af13bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045259"
---
# <a name="bidi-control-attribute"></a>Attribut de contrôle BiDi

Il s’agit d’une combinaison de l’ordre de lecture de droite à gauche [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)et [LeftScroll](leftscroll-control-attribute.md) attributs.

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



| Decimal | Valeur hexadécimale | Constante                       |
|---------|-------------|--------------------------------|
| 224     | 0x000000E0  | **msidbControlAttributesBiDi** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit BiDi dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



