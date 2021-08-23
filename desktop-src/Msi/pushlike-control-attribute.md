---
description: Si ce bit est défini sur une case à cocher ou un groupe de cases d’option, le bouton est dessiné avec l’apparence d’un bouton de commande, mais sa logique reste la même. Si le bit n’est pas défini, les contrôles sont dessinés dans leur style habituel.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Attribut de contrôle PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692478"
---
# <a name="pushlike-control-attribute"></a>Attribut de contrôle PushLike

Si ce bit est défini sur une case à cocher ou un groupe de cases d’option, le bouton est dessiné avec l’apparence d’un bouton de commande, mais sa logique reste la même. Si le bit n’est pas défini, les contrôles sont dessinés dans leur style habituel.

## <a name="valid-controls"></a>Contrôles valides

[Case à cocher](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit PushLike dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



