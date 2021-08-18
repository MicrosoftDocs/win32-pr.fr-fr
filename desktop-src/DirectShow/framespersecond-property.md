---
description: La propriété FramesPerSecond récupère la fréquence d’images vidéo pour le titre du DVD actuel.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Propriété FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a883f031680a57711fa092f29bc9ecbd76cb1a017c03f80337959050e62cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015667"
---
# <a name="framespersecond-property"></a>Propriété FramesPerSecond

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `FramesPerSecond` propriété récupère la fréquence d’images vidéo pour le titre du DVD actuel.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant la fréquence d’images vidéo ; 25 ou 30 images par seconde.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Les signaux vidéo NTSC sont affichés à 30 images par seconde. La PAL est affichée à 25 images par seconde. Un disque est encodé pour être lu sur NTSC ou PAL, mais ne peut pas être lu sur les deux.

 

 



