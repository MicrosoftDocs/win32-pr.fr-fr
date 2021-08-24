---
description: Cet attribut spécifie si le contrôle donné est activé ou désactivé. La plupart des contrôles apparaissent gris lorsqu’ils sont désactivés.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Attribut de contrôle activé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40de14ac0205c52cce46c6050de0282e62df90d50f3bcdeb576771c9107ffc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763919"
---
# <a name="enabled-control-attribute"></a>Attribut de contrôle activé

Cet attribut spécifie si le contrôle donné est activé ou désactivé. La plupart des contrôles apparaissent gris lorsqu’ils sont désactivés.

Si ce bit est défini, le contrôle est créé comme activé.

Si ce bit n’est pas défini, le contrôle est créé comme étant désactivé.

## <a name="valid-controls"></a>Contrôles valides

Tous les contrôles. L’apparence de certains contrôles qui ne sont pas associés à une propriété, tels que des bitmaps et des icônes, n’est pas affectée par la définition de cet attribut.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Remarques

Vous pouvez également utiliser la [table ControlCondition](controlcondition-table.md) pour désactiver ou activer un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle.

Vous pouvez également activer ou désactiver un contrôle en abonnant le contrôle à un [ControlEvent,](control-events.md). Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de l’événement dans la colonne d’événement de la [table EventMapping](eventmapping-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



