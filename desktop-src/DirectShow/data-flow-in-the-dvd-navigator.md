---
description: Flow de données dans le navigateur DVD
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Flow de données dans le navigateur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e649edfacf0a1fad56cfbe8e73a5e1e9aaf099b9c17463858bf776ab06605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953358"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Flow de données dans le navigateur DVD

Le navigateur DVD comporte des méthodes pour arrêter et suspendre la lecture. Ces méthodes sont similaires, mais pas identiques, aux méthodes **Stop** et **Pause** dans [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Voici la différence entre les deux :

-   Les méthodes **IDvdControl2** changent ce que le navigateur DVD lit à partir du disque. Elles ne modifient pas l’état du graphique.
-   Les méthodes **IMediaControl** modifient l’état du graphique. Ils ne changent pas ce que le navigateur DVD lit à partir du disque. (Il existe une exception importante, décrite dans la section suivante, associée à la méthode **Stop** .)

Par exemple, [**IDvdControl2 ::P méthode ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) émet la commande « pause on » de l’annexe J \_ , mais n’interrompt pas le graphique de filtre. La méthode [**IMediaControl ::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) , en revanche, interrompt le graphique mais n’émet pas de commande de DVD.

En général, utilisez les méthodes **IMediaControl ::P ause** et **Stop** à la place des méthodes **IDvdControl2** correspondantes. Les méthodes **IMediaControl** présentent des latences très faibles, tandis que les méthodes **IDvdControl2** peuvent avoir jusqu’à deux secondes de latence.

Arrêt de la lecture

Le comportement de [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) dépend d’un indicateur que vous pouvez définir avec la méthode [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

-   Si l' \_ indicateur RESETONSTOP DVD est **false**, **IMediaControl :: Stop** arrête le graphique, mais ne modifie pas le domaine du navigateur DVD. Lorsque vous appelez à nouveau exécuter, la lecture reprend à partir de la position actuelle.
-   Si \_ le DVD ResetOnStop a la **valeur true**, **IMediaControl :: Stop** provoque la réinitialisation du navigateur DVD. Quand vous appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) à nouveau, le navigateur DVD est lu à partir du premier domaine Play, comme si vous aviez inséré le DVD pour la première fois.

L' \_ indicateur RESETONSTOP DVD est **true** par défaut, pour la compatibilité avec les applications plus anciennes. En règle générale, toutefois, vous devez remplacer la valeur par défaut et définir l’indicateur sur **false**. En effet, certains événements peuvent entraîner l’arrêt du graphique pendant la lecture. Par exemple, si la résolution d’affichage change, le graphique de filtre s’arrête, reconnecte le convertisseur vidéo et redémarre. Si le DVD \_ ResetOnStop a la **valeur true**, la lecture redémarrera à partir du début du disque. Ce n’est probablement pas ce que l’utilisateur attend.

Par conséquent, au début de votre application, appelez la fonction **SetOption** avec DVD \_ ResetOnStop défini sur **false**. Si vous souhaitez arrêter la lecture et la reprendre à partir du même emplacement, appelez **IMediaControl :: Stop** ou **IMediaControl ::P ause**. Si vous souhaitez arrêter la lecture et réinitialiser le disque, appelez **SetOption** avec DVD \_ ResetOnStop égal à **true**, puis appelez **IMediaControl :: Stop**; Enfin, appelez la fonction **SetOption** à nouveau et réinitialisez le DVD \_ ResetOnStop sur **false**.

Suspension de la lecture

Si vous transmettez au navigateur DVD une commande alors que le graphique est en pause, la commande peut ne pas se terminer tant que le graphique n’est pas réexécuté. Dans certains cas, cela peut provoquer un blocage dans votre application. Pour éviter les blocages, vous devez suivre deux règles :

-   Pendant la suspension, n’émettez pas plus d’une commande de DVD asynchrone.
-   Pendant la suspension, ne bloquez pas le thread d’interface utilisateur de l’application ou le thread qui modifie l’état du graphique.

La deuxième règle mérite d’être examinée plus en détail. Voici quelques scénarios spécifiques qui peuvent provoquer un interblocage :

-   **Scénario**: lorsqu’il est suspendu, l’application émet une commande DVD avec l’indicateur de blocage. Cela peut provoquer un blocage si le thread qui émet la commande DVD est le même que celui qui émet la commande Run. La commande DVD est bloquée jusqu’à ce que le graphique s’exécute, mais le graphique ne peut pas s’exécuter tant que la commande n’est pas terminée.

    **Recommandation**: émettez la commande DVD sur un thread de travail distinct ou n’utilisez pas l’indicateur de blocage.

-   **Scénario**: lorsqu’il est suspendu, l’application émet une commande de DVD, puis appelle [**IDvdCmd :: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) sur l’objet de commande. Cette situation est équivalente à l’exemple précédent. Si vous appelez **Wait** à partir du thread d’interface utilisateur, le thread d’interface utilisateur ne peut pas exécuter le graphique tant que la méthode **Wait** n’est pas débloquée, mais la méthode **Wait** n’est pas débloquée tant que le graphique n’est pas exécuté.

    **Recommandation**: appelez **Wait** sur un thread de travail.

-   **Scénario**: pendant que le graphique est en cours d’exécution, l’application émet une commande de DVD avec l’indicateur de blocage, puis appelle la suspension d’un autre thread. Il s’agit d’une condition de concurrence possible, car le graphique peut s’interrompre avant l’émission de la commande. Si l’un des deux threads est le thread d’interface utilisateur, vous pouvez provoquer un blocage semblable aux deux exemples précédents. Cet exemple illustre l’importance de l’écriture de code thread-safe si votre application utilise plusieurs threads.

    **Recommandation**: Si vous utilisez des threads de travail, assurez-vous que votre code est thread-safe.

-   **Scénario**: lorsqu’il est suspendu, l’application désactive la commande exécuter à partir de l’interface utilisateur, puis émet une commande DVD asynchrone. Ce cas de figure n’est pas strictement un blocage, car le thread d’application est toujours en cours d’exécution. Toutefois, l’utilisateur ne peut plus exécuter le graphique et par conséquent, la commande ne se termine pas.

    **Recommandation**: lors de la suspension, laissez toujours la commande exécuter activée.

Recherche d’un DVD à une heure spécifiée

Pour rechercher précisément une heure spécifique sur un disque, appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Appelez ensuite [**IDvdControl2 ::P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime), en spécifiant l’heure et en définissant *dwFlags* sur l' \_ indicateur de cmd DVD \_ \_ Flush.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



