---
description: La propriété CurrentVolume récupère le numéro de volume du répertoire racine actuel.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriété CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516335"
---
# <a name="currentvolume-property"></a>Propriété CurrentVolume

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentVolume` propriété récupère le numéro de volume pour le répertoire racine actuel.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le volume DVD actuel. Si un disque fait partie d’un ensemble de plusieurs volumes, la valeur entière doit être supérieure à zéro.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



