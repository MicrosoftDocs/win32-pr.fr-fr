---
description: Les types de compteurs d’algorithme de minuterie sont basés sur la quantité d’utilisation accrue de l’objet de performance sur une période d’échantillonnage.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Types de compteurs de l’algorithme Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e3a606babb005eca7f01f75f735cd6d6a9da29c9c1427c56614c318f9465f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554013"
---
# <a name="timer-algorithm-counter-types"></a>Types de compteurs de l’algorithme Timer

Les types de compteurs d’algorithme de minuterie sont basés sur la quantité d’utilisation accrue de l’objet de performance sur une période d’échantillonnage. Les données de compteur sont une mesure de Quantum en plus de l’activité totale d’un objet jusqu’au moment où l’échantillon a eu lieu. La différence entre les deux exemples indique la durée totale pendant laquelle l’objet est actif pendant la période d’échantillonnage.

La division par la période d’échantillonnage entraîne une proportion de temps pendant lequel l’objet est actif pendant une période donnée. La division par le nombre d’interruptions d’interrogation internes détermine l’utilisation moyenne entre les exemples d’interrogation.

Par exemple, la propriété **AvgDiskSecPerRead** dans la classe [**Win32 \_ PerfRawData \_ Perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) utilise le type de **\_ \_ minuteur de performances moyenne** . Il calcule la durée moyenne en secondes d’une lecture de données à partir du disque et requiert la propriété de base **AvgDiskSecPerRead \_ base**. Contrairement **au \_ \_ minuteur de compteur de performances**, la base de minuterie moyenne représente un nombre cumulé d’opérations, et les données de compteur sont une valeur de temps d’exécution, ce qui signifie que lorsqu’elles sont divisées par la base de temps, elle génère la durée totale de toutes les opérations, en secondes.



| Type de compteur, constante                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_minuteur de compteur de performances \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 541132032<br/>             | Durée moyenne pendant laquelle un composant est actif sous la forme d’un pourcentage de la durée totale de l’échantillonnage.<br/>                                                                                                                                                                                                                                                                                                         |
| [\_ \_ inventaire du compteur de performances \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 557909248<br/>        | Pourcentage de temps moyen observé pendant l’intervalle échantillon pendant lequel l’objet n’est pas actif. Ce type de compteur est identique à **perf \_ 100NSEC \_ Timer \_** , sauf qu’il mesure le temps en unités de graduations de la minuterie des performances système plutôt qu’en unités de 100 ns.<br/>                                                                                                                       |
| [\_minuteur de performance moyen \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 805438464<br/>             | Durée moyenne d’exécution d’un processus ou d’une opération. Ce type de compteur affiche un rapport entre le temps total écoulé de l’intervalle échantillon et le nombre de processus ou d’opérations terminés au cours de cette période.<br/> Ce type de compteur requiert une propriété de base avec une **\_ \_ base moyenne de performances** comme type de compteur.<br/>                                                                         |
| [\_ \_ Minuteur 100NSEC perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 542180608<br/>             | Temps d’activité d’un composant sous la forme d’un pourcentage du temps total écoulé en unités de 100 ns de l’intervalle échantillon.<br/>                                                                                                                                                                                                                                                                          |
| [PERF \_ 100NSEC \_ minuteur \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 558957824<br/>        | Pourcentage de temps pendant lequel l’objet n’était pas utilisé. Ce type de compteur est le même que celui du **\_ \_ minuteur de compteur \_ de performances** , sauf qu’il mesure le temps en unités de 100 ns plutôt que dans les battements du minuteur de performances système.<br/>                                                                                                                                                                                   |
| [compteur de performances \_ \_ multiple \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 574686464<br/>      | Durée d’activité d’un ou plusieurs composants sous forme de pourcentage du temps total de l’intervalle échantillon. Ce type de compteur diffère de **perf \_ 100NSEC \_ multiple \_ Timer** en ce qu’il mesure le temps en unités de graduations de la minuterie des performances système, plutôt qu’en unités de 100 ns.<br/> Ce type de compteur requiert une propriété de base avec le type de compteur de **\_ \_ \_ base multiple de compteur de performances** .<br/>        |
| [compteur de performances ( \_ \_ plusieurs \_ minuteurs) \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 591463680<br/> | Durée d’inactivité d’un ou plusieurs composants en pourcentage du temps total de l’intervalle échantillon. Ce type de compteur diffère de **perf \_ 100NSEC \_ multi \_ Timer \_** en ce qu’il mesure le temps en unités de graduations de la minuterie des performances système, plutôt qu’en unités de 100 ns.<br/> Ce type de compteur requiert une propriété de base avec le type de compteur de **\_ \_ \_ base multiple de compteur de performances** .<br/> |
| [\_ \_ \_ MINUTEur 100NSEC perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 575735040<br/>      | Ce type de compteur affiche la durée d’activité d’un ou plusieurs composants sous forme de pourcentage du temps total (unités de 100 ns) de l’intervalle échantillon.<br/> Ce type de compteur requiert une propriété de base avec le type de compteur de **\_ \_ \_ base multiple de compteur de performances** .<br/>                                                                                                                                     |
| [PERF \_ 100NSEC \_ multi- \_ Timer \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 592512256<br/> | Durée d’inactivité d’un ou plusieurs composants en pourcentage du temps total de l’intervalle échantillon. Les compteurs de ce type mesurent le temps en unités de 100 ns.<br/> Ce type de compteur requiert une propriété de base avec le type de compteur de **\_ \_ \_ base multiple de compteur de performances** .<br/>                                                                                                                          |
| [\_ \_ minuteur de temps obj de perf \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Décimal 543229184<br/>           | Minuteur 64 bits dans les unités spécifiques à l’objet.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

