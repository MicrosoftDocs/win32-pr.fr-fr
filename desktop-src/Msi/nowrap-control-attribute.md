---
description: Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne. Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (&\# 0034 ;... &\# 0034 ;) est inséré à la fin pour indiquer la troncation. Si ce bit n’est pas défini, le texte est renvoyé à la ligne.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attribut de contrôle nowrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ef67a58dd0898b4c1e6d1577d35d67e8810649d49425087fecc3e0b3518cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519639"
---
# <a name="nowrap-control-attribute"></a>Attribut de contrôle nowrap

Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne. Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (« ... ») sont insérés à la fin pour indiquer la troncation. Si ce bit n’est pas défini, le texte est renvoyé à la ligne.

## <a name="valid-controls"></a>Contrôles valides

[Text](text-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit nowrap dans la colonne Attributes de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



