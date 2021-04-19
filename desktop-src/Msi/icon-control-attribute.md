---
description: Si ce bit est défini, le texte est remplacé par une image d’icône et la colonne de texte dans la table de contrôle est une clé étrangère dans la table binaire.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Icon, attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527353"
---
# <a name="icon-control-attribute"></a>Icon, attribut de contrôle

Si ce bit est défini, le texte est remplacé par une image d’icône et la colonne de texte dans la [table de contrôle](control-table.md) est une clé étrangère dans la [table binaire](binary-table.md).

Si ce bit n’est pas défini, le texte du contrôle est spécifié dans la colonne text de la [table de contrôle](control-table.md).

## <a name="valid-controls"></a>Contrôles valides

[CheckBox](checkbox-control.md)

[Boutons](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez les bits d’icône dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

La colonne de texte de la table de contrôle est utilisée comme clé étrangère de la [table binaire](binary-table.md). par conséquent, le contrôle ne peut pas contenir à la fois une image d’icône et du texte.

Ne définissez pas à la fois l’icône et les bits de [bitmap](bitmap-control-attribute.md) .

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



