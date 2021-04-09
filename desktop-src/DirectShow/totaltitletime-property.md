---
description: La propriété TotalTitleTime récupère le temps de lecture total pour le titre actuel.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriété TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865789"
---
# <a name="totaltitletime-property"></a>Propriété TotalTitleTime

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `TotalTitleTime` propriété récupère le temps de lecture total pour le titre actuel.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valeur renvoyée

Retourne la durée d’exécution totale du titre actuel sous la forme d’une chaîne au format « hh : mm : SS : FF ».

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. La chaîne retournée aura une longueur de 11 caractères au format « hh : mm : SS : FF » (heures, minutes, secondes, frames).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



