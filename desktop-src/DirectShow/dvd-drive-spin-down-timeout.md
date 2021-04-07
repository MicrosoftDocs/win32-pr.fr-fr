---
description: Délai d’attente de Spin Down du lecteur DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Délai d’attente de Spin Down du lecteur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846606"
---
# <a name="dvd-drive-spin-down-timeout"></a>Délai d’attente de Spin Down du lecteur DVD

Sur les ordinateurs portables, pour économiser la batterie, il peut être souhaitable de réduire la durée pendant laquelle un lecteur de DVD continue de tourner une fois que l’utilisateur a suspendu la lecture. Par défaut, le navigateur DVD garde le disque tourner pendant deux minutes. Cette valeur peut être modifiée dans le Registre Windows sous cette clé :


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



where


```
Sec
```



durée de Spin Down en secondes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annexes](appendixes.md)
</dt> </dl>

 

 



