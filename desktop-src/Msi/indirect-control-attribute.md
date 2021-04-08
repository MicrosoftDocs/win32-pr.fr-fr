---
description: L’attribut de contrôle indirect spécifie si la valeur affichée ou modifiée par ce contrôle est référencée indirectement.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Attribut de contrôle indirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d0c183f586c197b14810e7176bce607ac3adaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864222"
---
# <a name="indirect-control-attribute"></a>Attribut de contrôle indirect

L’attribut de contrôle indirect spécifie si la valeur affichée ou modifiée par ce contrôle est référencée indirectement. Si ce bit est défini, le contrôle affiche ou modifie la valeur de la propriété qui a l’identificateur figurant dans la colonne propriété de la [table de contrôle](control-table.md). Si ce bit n’est pas défini, le contrôle affiche ou modifie la valeur de la propriété dans la colonne propriété de la table de contrôle.

## <a name="valid-controls"></a>Contrôles valides

Tous les contrôles actifs.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Notes

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



