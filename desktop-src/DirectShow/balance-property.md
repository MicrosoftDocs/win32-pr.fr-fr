---
description: La propriété balance définit ou récupère le solde du haut-parleur pour la sortie du flux audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propriété balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512872"
---
# <a name="balance-property"></a>Propriété balance

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Balance` propriété définit ou récupère le solde du haut-parleur pour la sortie du flux audio.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant les niveaux de solde. La plage d’entrée autorisée est comprise entre-10 000 et 10 000. La valeur 0 définit un équilibre neutre, c’est-à-dire que les haut-parleurs gauche et droit reçoivent le même signal audio amplitude.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture avec une valeur par défaut de 0, ce qui signifie que les deux enceintes reçoivent des signaux audio équivalents. Comme avec la propriété [**volume**](volume-property.md) , Units correspond à 0,01 décibels (multiplié par-1 lorsque


```
iBalance
```



est une valeur positive). Par exemple, la valeur 1000 indique 10 dB sur le canal droit et 90 dB sur le canal de gauche.

 

 



