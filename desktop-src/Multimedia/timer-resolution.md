---
title: Résolution de la minuterie
description: Résolution de la minuterie
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- minuteurs multimédias, résolution
- minuteries, résolution
- résolution minimale de la minuterie
- résolution maximale de la minuterie
- minuteurs multimédias, résolution maximale
- minuteries, résolution maximale
- minuteurs multimédias, résolution minimale
- minuteries, résolution minimale
- timeGetDevCaps fonction)
- timeBeginPeriod fonction)
- timeEndPeriod fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369340"
---
# <a name="timer-resolution"></a>Résolution de la minuterie

Pour déterminer les résolutions minimale et maximale des minuteries prises en charge par les services du minuteur, utilisez la fonction [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) . Cette fonction remplit les membres **wPeriodMin** et **wPeriodMax** de la structure [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) avec les résolutions minimale et maximale. cette plage peut varier d’un ordinateur à l’autre Windows plateformes.

Une fois que vous avez déterminé les résolutions minimale et maximale disponibles du minuteur, vous devez définir la résolution minimale que votre application doit utiliser. Utilisez les fonctions [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) pour définir et effacer cette résolution. Vous devez faire correspondre chaque appel à **timeBeginPeriod** avec un appel à **timeEndPeriod**, en spécifiant la même résolution minimale dans les deux appels. Une application peut effectuer plusieurs appels **timeBeginPeriod** , à condition que chaque appel corresponde à un appel à **timeEndPeriod**.

Dans [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) et [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), le paramètre *uPeriod* indique la résolution de minuteur minimale, en millisecondes. Vous pouvez spécifier n’importe quelle valeur de résolution de la minuterie dans la plage prise en charge par la minuterie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des minuteurs multimédias](about-multimedia-timers.md)
</dt> </dl>

 

 




