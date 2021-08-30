---
description: Délai d’attente de Spin Down du lecteur DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Délai d’attente de Spin Down du lecteur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6283f0846ac374ee9f059b6ac712209ceb0a925b904fcb941b5cf14f0e36d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051879"
---
# <a name="dvd-drive-spin-down-timeout"></a>Délai d’attente de Spin Down du lecteur DVD

Sur les ordinateurs portables, pour économiser la batterie, il peut être souhaitable de réduire la durée pendant laquelle un lecteur de DVD continue de tourner une fois que l’utilisateur a suspendu la lecture. Par défaut, le navigateur DVD garde le disque tourner pendant deux minutes. cette valeur peut être modifiée dans le registre Windows sous cette clé :


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

 

 



