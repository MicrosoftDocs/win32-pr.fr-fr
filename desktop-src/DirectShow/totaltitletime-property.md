---
description: La propriété TotalTitleTime récupère le temps de lecture total pour le titre actuel.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriété TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650849"
---
# <a name="totaltitletime-property"></a>Propriété TotalTitleTime

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `TotalTitleTime` propriété récupère le temps de lecture total pour le titre actuel.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valeur renvoyée

Retourne la durée d’exécution totale du titre actuel sous la forme d’une chaîne au format « hh : mm : SS : FF ».

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. La chaîne retournée aura une longueur de 11 caractères au format « hh : mm : SS : FF » (heures, minutes, secondes, frames).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



