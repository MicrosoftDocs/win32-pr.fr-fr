---
description: Un fichier d’icône peut contenir plusieurs tailles différentes de la même image d’icône.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Icon, attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034397"
---
# <a name="iconsize-control-attribute"></a>Icon, attribut de contrôle

Un fichier d’icône peut contenir plusieurs tailles différentes de la même image d’icône. Ces bits spécifient la taille de l’image d’icône à charger. Si aucun des bits n’est défini, la première image est chargée. Si seul **msidbControlAttributesIconSize16** est défini, la première image de 16x16 est chargée. Si seul le **msidbControlAttributesIconSize32** est défini, la première image 32x32 est chargée. Si **msidbControlAttributesIconSize48** est défini, la première image 48 est chargée.

## <a name="valid-controls"></a>Contrôles valides

[CheckBox](checkbox-control.md)

[Icône](icon-control.md)

[Boutons](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Description                          |
|---------|-------------|--------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4 194 304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez les bits d’icône dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Si le bit [FixedSize](fixedsize-control-attribute.md) n’est pas défini, l’image chargée est réduite ou étirée pour s’ajuster au contrôle d’icône. Si le bit [FixedSize](fixedsize-control-attribute.md) est défini et que l’image chargée est plus petite que le contrôle Icon, l’image est centrée à l’intérieur du contrôle. Si le bit [FixedSize](fixedsize-control-attribute.md) est défini et que l’image chargée est plus grande que le contrôle Icon, l’image est réduite pour s’ajuster au contrôle.

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



