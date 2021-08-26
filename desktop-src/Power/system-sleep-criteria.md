---
description: Tant que le système détermine l’activité de l’utilisateur ou de l’application, il n’entre pas en mode veille.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Critères de veille du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b93b0eb1a55d156a9d75b51ef826c85eabd28b29789cf50bb7f0fd7b5fee90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032819"
---
# <a name="system-sleep-criteria"></a>Critères de veille du système

Tant que le système détermine l’activité de l’utilisateur ou de l’application, il n’entre pas en mode veille. Le système peut détecter certaines activités, telles que les entrées d’utilisateur ou les communications réseau. Toutefois, il existe d’autres activités que le système ne peut pas détecter. Par exemple, une application de présentation requiert l’affichage de l’écran. Toutefois, il peut sembler que l’application est inactive pendant la présentation, provoquant ainsi l’arrêt de l’affichage par le système.

Pour informer le système que votre application est occupée, utilisez la fonction [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) . Cette fonction empêche le système d’entrer en mode veille ou de désactiver l’affichage pendant que l’application est en cours d’exécution.

Les applications de présentation et multimédias doivent appeler la fonction [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) avec l' **\_ affichage es \_ requis** pour que le système sache qu’il ne doit pas mettre le périphérique d’affichage en veille. Les applications de gestion des événements, telles que les outils de gestion des télécopies entrantes, doivent appeler **SetThreadExecutionState** avec le **\_ système es \_ requis**, gérer l’événement, puis effacer l’indicateur afin que le système puisse revenir en mode veille. Notez que la plupart des applications de productivité n’ont pas besoin d’utiliser **SetThreadExecutionState** , car le système peut généralement déterminer l’activité par entrée d’utilisateur.

Pour maintenir le temps depuis la dernière entrée utilisateur, le système utilise un minuteur d’affichage inactif et un minuteur d’inactivité du système. Le système compare les temps d’inactivité aux valeurs configurées dans le mode de gestion de l’alimentation. Si la valeur du minuteur d’inactivité de l’affichage est supérieure à la valeur du délai d’attente d’affichage et qu’aucun thread n’a demandé l’affichage en appelant [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) avec l' **\_ affichage es \_ requis**, le système met hors tension l’affichage. De même, si le délai d’inactivité du système est supérieur à la valeur du délai d’attente du système et qu’aucune application n’a demandé le système en appelant **SetThreadExecutionState** avec le **\_ système es \_ requis**, le système passe en mode veille.

Le système gère le nombre d’applications qui ont appelé [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate). Le système effectue le suivi de chaque thread qui appelle **SetThreadExecutionState** et ajuste le compteur en conséquence. Si ce compteur atteint zéro et qu’il n’y a pas d’entrée utilisateur, le système passe en mode veille.

Si la puissance est faible, une application peut demander l’intervention de l’utilisateur ou demander que le système s’interrompt. Vous pouvez suspendre le fonctionnement du système à l’aide de la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

Si le système sort de veille automatiquement ([PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)), aucun minuteur n’est pertinent. Pour plus d’informations, consultez [événements de mise en éveil du système](system-wake-up-events.md).

## <a name="entering-sleep"></a>Entrée en mode veille

Lorsque le système passe en mode veille, il conserve automatiquement l’état de l’ensemble du système et de toutes les applications. Par conséquent, la plupart des applications n’ont pas besoin d’effectuer d’action particulière. Les applications qui doivent effectuer des actions spécifiques avant que les transitions système puissent s’inscrire aux événements d’alimentation.

Lorsque le système envoie un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) , chaque application dispose de deux secondes pour effectuer toutes les actions nécessaires avant que le système ne démarre la transition vers le mode veille. Les applications doivent limiter l’action qu’elles prennent en réponse à cet événement pour s’assurer qu’elles terminent toutes les opérations dans le temps alloué.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> <dt>

[Événements de mise en éveil du système](system-wake-up-events.md)
</dt> </dl>

 

 



