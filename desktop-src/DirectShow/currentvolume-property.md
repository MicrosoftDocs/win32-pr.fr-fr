---
description: La propriété CurrentVolume récupère le numéro de volume du répertoire racine actuel.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriété CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654601"
---
# <a name="currentvolume-property"></a>Propriété CurrentVolume

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentVolume` propriété récupère le numéro de volume pour le répertoire racine actuel.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le volume DVD actuel. Si un disque fait partie d’un ensemble de plusieurs volumes, la valeur entière doit être supérieure à zéro.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



