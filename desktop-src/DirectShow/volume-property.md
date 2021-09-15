---
description: La propriété volume définit ou récupère le volume du haut-parleur pour la sortie du flux audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238895"
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

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture avec 0 comme valeur par défaut. Le volume complet est 0, et 10 000 est un silence ; l’échelle est logarithmique. Multipliez le niveau de décibel souhaité par 100 (par exemple 10 000 = 100 dB).

 

 



