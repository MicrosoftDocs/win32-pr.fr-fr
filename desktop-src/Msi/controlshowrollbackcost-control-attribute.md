---
description: Cet attribut spécifie si les fichiers de sauvegarde de restauration sont inclus dans les coûts affichés par le contrôle VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Attribut de contrôle ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867297"
---
# <a name="controlshowrollbackcost-control-attribute"></a>Attribut de contrôle ControlShowRollbackCost

Cet attribut spécifie si les fichiers de sauvegarde de restauration sont inclus dans les coûts affichés par le [contrôle VolumeCostList](volumecostlist-control.md).

Si ce bit est défini et que la propriété [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, les fichiers de sauvegarde de restauration sont inclus dans le coût affiché par le [contrôle VolumeCostList](volumecostlist-control.md).

Si ce bit n’est pas défini et que la propriété [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, les fichiers de restauration de sauvegarde ne sont pas inclus dans le coût affiché par le [contrôle VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Contrôles valides

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 4 194 304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Notes

Cet attribut de contrôle est ignoré si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou F.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, le coût de la restauration, les fichiers de sauvegarde sont inclus.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou la propriété [**disablerollback**](-disablerollback.md) = 1, le coût de la restauration, les fichiers de sauvegarde ne sont pas inclus.

 

 



