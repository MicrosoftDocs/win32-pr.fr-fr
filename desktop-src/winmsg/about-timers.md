---
description: Cette rubrique explique comment créer, identifier, définir et supprimer des minuteries.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: À propos des minuteries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364460"
---
# <a name="about-timers"></a>À propos des minuteries

Cette rubrique explique comment créer, identifier, définir et supprimer des minuteries. Une application utilise un minuteur pour planifier un événement pour une fenêtre après l’expiration d’un délai spécifié. Chaque fois que l’intervalle spécifié (ou la valeur du délai d’attente) d’un minuteur est écoulé, le système avertit la fenêtre associée à la minuterie. Étant donné que la précision d’un minuteur dépend de la fréquence d’horloge du système et de la fréquence à laquelle l’application récupère les messages de la file d’attente de messages, la valeur du délai d’attente est uniquement approximative.

Cette rubrique comprend les sections suivantes.

-   [Opérations du minuteur](#timer-operations)
-   [Minuteur de haute résolution](#high-resolution-timer)
-   [Objets Timer waitables](#waitable-timer-objects)
-   [Rubriques connexes](#related-topics)

## <a name="timer-operations"></a>Opérations du minuteur

Les applications créent des minuteurs à l’aide de la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Une nouvelle minuterie commence à chronométrer l’intervalle dès sa création. Une application peut modifier la valeur du délai d’attente d’un minuteur à l’aide de **SetTimer** et peut détruire un minuteur à l’aide de la fonction [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) . Pour utiliser efficacement les ressources système, les applications doivent détruire les minuteurs qui ne sont plus nécessaires.

Chaque minuteur possède un identificateur unique. Lorsque vous créez un minuteur, une application peut spécifier un identificateur ou faire en sorte que le système crée une valeur unique. Le premier paramètre d’un message du [**\_ minuteur WM**](wm-timer.md) contient l’identificateur de la minuterie qui a publié le message.

Si vous spécifiez un handle de fenêtre dans l’appel à [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer), l’application associe le minuteur à cette fenêtre. Chaque fois que la valeur du délai d’attente de la minuterie s’écoule, le système publie un message de [**\_ minuteur WM**](wm-timer.md) dans la fenêtre associée au minuteur. Si aucun handle de fenêtre n’est spécifié dans l’appel à **SetTimer**, l’application qui a créé le minuteur doit surveiller sa file d’attente de messages pour les messages **\_ du minuteur WM** et les distribuer à la fenêtre appropriée. Si vous spécifiez une fonction de rappel [**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc) , la procédure de fenêtre par défaut appelle la fonction de rappel lors du traitement du **\_ minuteur WM**. Par conséquent, vous devez distribuer les messages dans le thread appelant, même si vous utilisez **TimerProc** au lieu de traiter le **\_ minuteur WM**.

Si vous souhaitez être averti quand un minuteur s’écoule, utilisez un minuteur qui est attendu. Pour plus d’informations, consultez la rubrique [objets Timer waitables](/windows/desktop/Sync/waitable-timer-objects).

## <a name="high-resolution-timer"></a>Minuteur High-Resolution

Un compteur est un terme général utilisé dans la programmation pour faire référence à une variable d’incrémentation. Certains systèmes incluent un compteur de performance haute résolution qui fournit des temps de haute résolution.

Si un compteur de performance haute résolution existe sur le système, vous pouvez utiliser la fonction [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) pour exprimer la fréquence, en nombre par seconde. La valeur du nombre dépend du processeur. Sur certains processeurs, par exemple, le nombre peut être le taux de cycle de l’horloge du processeur.

La fonction [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) récupère la valeur actuelle du compteur de performance haute résolution. En appelant cette fonction au début et à la fin d’une section de code, une application utilise essentiellement le compteur comme un minuteur haute résolution. Par exemple, supposons que [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) indique que la fréquence du compteur de performance haute résolution est de 50 000 nombres par seconde. Si l’application appelle **QueryPerformanceCounter** juste avant et juste après la section de code à chronométrer, les valeurs de compteur peuvent être respectivement 1500 et 3500. Ces valeurs indiquent que .04 secondes (2000) s’est écoulée pendant l’exécution du code.

## <a name="waitable-timer-objects"></a>Objets Timer waitables

Un objet de minuteur qui peut être attendu est un objet de synchronisation dont l’État est défini sur signalé lorsque l’heure d’échéance spécifiée arrive. Il existe deux types de minuteurs qui peuvent être créés : Manuel-réinitialisation et synchronisation. Un minuteur de l’un des deux types peut également être un minuteur périodique.

Un thread utilise la fonction [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ou [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) pour créer un objet Timer. Le thread de création spécifie si la minuterie est un minuteur de réinitialisation manuelle ou un minuteur de synchronisation. Le thread de création peut spécifier un nom pour l’objet de minuteur. Les threads d’autres processus peuvent ouvrir un handle vers une minuterie existante en spécifiant son nom dans un appel à la fonction [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Tout thread avec un handle d’objet Timer peut utiliser l’une des fonctions Wait pour attendre que l’état du minuteur soit défini comme signalé.

Pour plus d’informations sur l’utilisation d’objets Timer waitables pour la synchronisation de threads, consultez [objets Timer waitables](/windows/desktop/Sync/waitable-timer-objects).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de minuteurs](using-timers.md)
</dt> </dl>

 

 
