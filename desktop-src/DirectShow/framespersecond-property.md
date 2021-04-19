---
description: La propriété FramesPerSecond récupère la fréquence d’images vidéo pour le titre du DVD actuel.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propriété FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515129"
---
# <a name="framespersecond-property"></a>Propriété FramesPerSecond

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `FramesPerSecond` propriété récupère la fréquence d’images vidéo pour le titre du DVD actuel.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant la fréquence d’images vidéo ; 25 ou 30 images par seconde.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Les signaux vidéo NTSC sont affichés à 30 images par seconde. La PAL est affichée à 25 images par seconde. Un disque est encodé pour être lu sur NTSC ou PAL, mais ne peut pas être lu sur les deux.

 

 



