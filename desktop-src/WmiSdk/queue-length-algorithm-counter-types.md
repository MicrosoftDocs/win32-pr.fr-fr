---
description: Les types de compteurs d’algorithmes de longueur de file d’attente incrémentent le nombre d’éléments dans une file d’attente à chaque intervalle d’échantillonnage, comme spécifié par la propriété de fréquence appropriée&\# 8212 ; Fréquence \_ PerfTime, et ainsi de suite.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Types de compteurs d’algorithmes de longueur de file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316536"
---
# <a name="queue-length-algorithm-counter-types"></a>Types de compteurs d’algorithmes de longueur de file d’attente

Les types de compteurs d’algorithmes de longueur de file d’attente incrémentent le nombre d’éléments dans une file d’attente à chaque intervalle d’échantillonnage, comme spécifié par la fréquence de propriété de fréquence appropriée \_ PerfTime, et ainsi de suite. Le résultat de la préproduction est divisé par le nombre d’échantillons pour produire la longueur moyenne de la file d’attente.

Par exemple, la propriété **AvgDiskQueueLength** dans le [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) qui utilise le \_ type de \_ compteur type de compteur de performances 100 NS \_ QUEUELEN \_ .



| @, Constante                                                                                                 | Description                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008<br/>            | Longueur moyenne d’une file d’attente vers une ressource dans le temps. Il affiche la différence entre les longueurs de file d'attente observées au cours des deux derniers intervalles échantillons divisée par la durée de l'intervalle.                       |
| [Performances \_ COMPTEUR \_ \_ QUEUELEN de \_ type grand](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))nombre décimal 4523264<br/>     | Longueur moyenne d’une file d’attente vers une ressource dans le temps. Les compteurs de ce type affichent la différence entre les longueurs de file d'attente observées au cours des deux derniers intervalles échantillons divisée par la durée de l'intervalle. |
| [Performances \_ COUNTER \_ 100 NS \_ QUEUELEN \_ type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840<br/>     | Longueur moyenne d’une file d’attente vers une ressource dans le temps en unités de 100 nanosecondes.                                                                                                                                        |
| [Performances \_ COUNTER \_ obj \_ Time \_ QUEUELEN \_ type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416<br/> | Heure à laquelle un objet se trouve dans une file d’attente.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

