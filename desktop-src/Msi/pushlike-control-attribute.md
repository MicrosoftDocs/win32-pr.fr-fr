---
description: Si ce bit est défini sur une case à cocher ou un groupe de cases d’option, le bouton est dessiné avec l’apparence d’un bouton de commande, mais sa logique reste la même. Si le bit n’est pas défini, les contrôles sont dessinés dans leur style habituel.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Attribut de contrôle PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531929"
---
# <a name="pushlike-control-attribute"></a>Attribut de contrôle PushLike

Si ce bit est défini sur une case à cocher ou un groupe de cases d’option, le bouton est dessiné avec l’apparence d’un bouton de commande, mais sa logique reste la même. Si le bit n’est pas défini, les contrôles sont dessinés dans leur style habituel.

## <a name="valid-controls"></a>Contrôles valides

[Case à cocher](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit PushLike dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



