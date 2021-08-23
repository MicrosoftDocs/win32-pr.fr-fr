---
description: La propriété volume définit ou récupère le volume du haut-parleur pour la sortie du flux audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632879"
---
# <a name="volume-property"></a>Volume, propriété

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Volume` propriété définit ou récupère le volume du haut-parleur pour la sortie du flux audio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valeur renvoyée

Retourne le niveau de volume en tant qu’atténuation en décibels sous la forme d’un entier.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture avec 0 comme valeur par défaut. Le volume complet est 0, et 10 000 est un silence ; l’échelle est logarithmique. Multipliez le niveau de décibel souhaité par 100 (par exemple 10 000 = 100 dB).

 

 



