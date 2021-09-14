---
description: Si ce bit est défini sur un contrôle, la propriété associée spécifiée dans la colonne de la propriété de la table de contrôle est un entier. Si ce bit n’est pas défini, la propriété est une valeur de chaîne.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Attribut de contrôle entier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012020"
---
# <a name="integer-control-attribute"></a>Attribut de contrôle entier

Si ce bit est défini sur un contrôle, la propriété associée spécifiée dans la colonne de la propriété de la [table de contrôle](control-table.md) est un entier. Si ce bit n’est pas défini, la propriété est une valeur de chaîne.

## <a name="valid-controls"></a>Contrôles valides

[CheckBox](checkbox-control.md)

[ComboBox](combobox-control.md)

[Modifier](edit-control.md)

[ListBox](listbox-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                          |
|---------|-------------|-----------------------------------|
| 16      | 0x00000010  | **msidbControlAttributesInteger** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit entier dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



