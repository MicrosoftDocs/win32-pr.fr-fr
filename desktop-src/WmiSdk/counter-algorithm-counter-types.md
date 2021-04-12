---
description: Les types de compteurs d’algorithmes de compteur peuvent calculer des taux ou des moyennes d’octets pour un échantillon ou sur une période de temps pour une opération particulière.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Types de compteurs d’algorithmes de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319674"
---
# <a name="counter-algorithm-counter-types"></a>Types de compteurs d’algorithmes de compteur

Les types de compteurs d’algorithmes de compteur peuvent calculer des taux ou des moyennes d’octets pour un échantillon ou sur une période de temps pour une opération particulière.

La propriété **AvgDiskBytesPerTransfer** de la classe [**Win32 \_ PerfRawData \_ Perfdisk \_ PHYSICALDISK**](/previous-versions//aa394308(v=vs.85)) utilise le nombre \_ moyen de performances \_ . Dans ce cas, le transfert est l’opération et le nombre cumulé d’octets envoyés correspond aux données du compteur. Pour les deux exemples, la Division de la différence entre les octets cumulés par la différence dans l’accumulation de transferts produira le nombre moyen d’octets par transfert pendant la période entre les exemples.

Les algorithmes de compteur suivants sont fournis :



| CounterType                                                                                              | Description                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ Décimale \_ en bloc moyenne](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073874176<br/>       | Nombre d’éléments traités, en moyenne, au cours d’une opération. Ce type de compteur affiche un rapport entre les éléments traités (tels que les octets envoyés) et le nombre d’opérations terminées, et requiert une propriété de base avec une \_ base moyenne de performances \_ comme type de compteur. |
| [Performances \_ Compteur \_ -nombre décimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696320<br/>     | Nombre moyen d’opérations effectuées au cours de chaque seconde de l’intervalle échantillon. .                                                                                                                                                                          |
| [Performances \_ EXEMPLE de \_ compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 4260864<br/>        | Nombre moyen d’opérations exécutées en une seconde. Ce type de compteur requiert une propriété de base avec l’exemple de base PERF de type de compteur \_ \_ .                                                                                                                   |
| [Performances \_ COMPTEUR \_ \_ nombre de blocs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 272696576<br/> | Nombre moyen d’opérations effectuées au cours de chaque seconde de l’intervalle échantillon. Ce type de compteur est identique au type de \_ compteur de compteur \_ de performances, mais il utilise des champs plus étendus pour prendre en charge des valeurs plus élevées.                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

