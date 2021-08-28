---
description: L’attribut de contrôle indirect spécifie si la valeur affichée ou modifiée par ce contrôle est référencée indirectement.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Attribut de contrôle indirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c679938a818fb8393958c35694f3c2b7f782c91fc2dfcf1ac04777553ec629c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996687"
---
# <a name="indirect-control-attribute"></a>Attribut de contrôle indirect

L’attribut de contrôle indirect spécifie si la valeur affichée ou modifiée par ce contrôle est référencée indirectement. Si ce bit est défini, le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la [table de contrôle](control-table.md). Si ce bit n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la table de contrôle.

## <a name="valid-controls"></a>Contrôles valides

Tous les contrôles actifs.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Remarques

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



