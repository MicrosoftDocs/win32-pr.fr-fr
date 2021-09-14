---
description: Si ce bit est défini, les éléments répertoriés dans le contrôle sont affichés dans un ordre spécifié. Si le bit n’est pas défini, les éléments sont affichés par ordre alphabétique.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Attribut de contrôle trié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233909"
---
# <a name="sorted-control-attribute"></a>Attribut de contrôle trié

Si ce bit est défini, les éléments répertoriés dans le contrôle sont affichés dans un ordre spécifié. Si le bit n’est pas défini, les éléments sont affichés par ordre alphabétique.

## <a name="valid-controls"></a>Contrôles valides

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[Contrôle ListView](listview-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesSorted** |



 

## <a name="remarks"></a>Notes

Pour trier les éléments d’une [zone de liste déroulante](combobox-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la colonne Order de la table de [zone de liste déroulante](combobox-table.md).

Pour trier les éléments d’une [zone de liste](listbox-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la colonne Order de la table de [zone de liste déroulante](combobox-table.md).

Pour trier les éléments dans un [ListView](listview-control.md), incluez le bit trié dans la colonne attributs de la [table de contrôle](control-table.md) et spécifiez l’ordre des éléments dans la table de zone de [liste déroulante](combobox-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



