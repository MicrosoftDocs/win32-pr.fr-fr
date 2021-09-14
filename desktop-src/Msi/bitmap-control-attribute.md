---
description: Si le bit de contrôle bitmap est défini, le texte du contrôle est remplacé par une image bitmap. La colonne de texte dans la table de contrôle est une clé étrangère dans la table binaire.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Attribut de contrôle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092366"
---
# <a name="bitmap-control-attribute"></a>Attribut de contrôle bitmap

Si le bit de contrôle bitmap est défini, le texte du contrôle est remplacé par une image bitmap. La colonne de texte dans la [table de contrôle](control-table.md) est une clé étrangère dans la [table binaire](binary-table.md).

Si ce bit n’est pas défini, le texte du contrôle est spécifié dans la colonne text de la [table Control](control-table.md).

## <a name="valid-controls"></a>Contrôles valides

[CheckBox](checkbox-control.md)

 

[Boutons](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit de bitmap dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

La colonne de texte de la table de contrôle est utilisée comme clé étrangère de la [table binaire](binary-table.md). par conséquent, le contrôle ne peut pas contenir à la fois une image d’icône et du texte.

Ne définissez pas à la fois l' [icône](icon-control-attribute.md) et les bits de bitmap.

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



