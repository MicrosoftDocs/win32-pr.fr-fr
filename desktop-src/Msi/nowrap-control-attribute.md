---
description: Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne. Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (&\# 0034 ;... &\# 0034 ;) est inséré à la fin pour indiquer la troncation. Si ce bit n’est pas défini, le texte est renvoyé à la ligne.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attribut de contrôle nowrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531991"
---
# <a name="nowrap-control-attribute"></a>Attribut de contrôle nowrap

Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne. Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (« ... ») sont insérés à la fin pour indiquer la troncation. Si ce bit n’est pas défini, le texte est renvoyé à la ligne.

## <a name="valid-controls"></a>Contrôles valides

[Text](text-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit nowrap dans la colonne Attributes de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



