---
description: Windows Sockets 2 introduit les e/s avec chevauchement et requiert que tous les fournisseurs de transport prennent en charge cette fonctionnalité.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Entrée/sortie avec chevauchement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641789"
---
# <a name="overlapped-inputoutput"></a>Entrée/sortie avec chevauchement

Windows Sockets 2 introduit les e/s avec chevauchement et requiert que tous les fournisseurs de transport prennent en charge cette fonctionnalité. Les e/s avec chevauchement peuvent être effectuées uniquement sur les sockets créés à l’aide de la fonction [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) avec l' \_ indicateur de chevauchement d’indicateur WSA \_ défini, et suivre le modèle établi dans Windows.

Pour la réception, un client utilise [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ou [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) pour fournir des mémoires tampons dans lesquelles les données doivent être reçues. Si une ou plusieurs mémoires tampons sont publiées avant le moment où les données ont été reçues par le réseau, il est possible que les données soient placées dans les mémoires tampons de l’utilisateur immédiatement à mesure qu’elles arrivent et, par conséquent, éviter l’opération de copie qui se produirait autrement. Si des données arrivent lorsque des mémoires tampons de réception ont déjà été publiées, elles sont copiées immédiatement dans les tampons de l’utilisateur. Si des données arrivent quand aucune mémoire tampon de réception n’a été publiée par l’application, le fournisseur de services accède au style synchrone de l’opération dans lequel les données entrantes sont mises en mémoire tampon jusqu’à ce que le client envoie un appel de réception et fournit ainsi une mémoire tampon dans laquelle les données peuvent être copiées. Une exception est si l’application a utilisé [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) pour définir la taille de la mémoire tampon de réception sur zéro. Dans ce cas, les protocoles Reliable autorisent uniquement la réception des données lorsque les tampons d’application ont été publiés, et les données sur les protocoles non fiables sont perdues.

Du côté de l’envoi, les clients utilisent [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) ou [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) pour fournir des pointeurs aux mémoires tampons remplies, puis décident de ne pas perturber les tampons jusqu’à ce que le réseau ait consommé le contenu de la mémoire tampon.

Les appels d’envoi et de réception superposés sont retournés immédiatement. Une valeur de retour égale à zéro indique que l’opération d’e/s s’est terminée immédiatement et que l’indication d’achèvement correspondante s’est déjà produite. Autrement dit, l’objet événement associé a été signalé ou la routine d’achèvement a été mise en file d’attente via [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Une valeur de retour de \_ l’erreur de socket couplée avec un code d’erreur d' \_ e/s de WSA \_ en attente indique que l’opération avec chevauchement a été correctement lancée et qu’une indication suivante sera fournie lorsque les mémoires tampons d’envoi ont été consommées ou lorsque les tampons de réception sont remplis. Tout autre code d’erreur indique que l’opération avec chevauchement n’a pas été lancée avec succès et qu’aucune indication d’achèvement n’est à venir.

Les opérations d’envoi et de réception peuvent être superposées. Les fonctions de réception peuvent être appelées plusieurs fois pour envoyer des tampons de réception en vue de la préparation des données entrantes, et les fonctions d’envoi peuvent être appelées plusieurs fois pour mettre en file d’attente l’envoi de plusieurs mémoires tampons. Notez que lorsqu’une série de mémoires tampons d’envoi avec chevauchement sera envoyée dans l’ordre indiqué, les indications d’achèvement correspondantes peuvent se produire dans un ordre différent. De même, du côté de la réception, les tampons sont remplis dans l’ordre dans lequel ils sont fournis, mais les indications de saisie semi-automatique peuvent se produire dans un ordre différent.

La fonctionnalité d’achèvement différé des e/s avec chevauchement est également disponible pour [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)).

## <a name="delivering-completion-indications"></a>Envoi d’indications d’achèvement

Les fournisseurs de services ont deux façons d’indiquer l’achèvement avec chevauchement : la définition d’un objet d’événement spécifié par le client ou l’appel d’une routine de saisie semi-automatique spécifiée par le client. Dans les deux cas, une structure de données, [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped), est associée à chaque opération avec chevauchement. Cette structure est allouée par le client et utilisée par elle pour indiquer l’objet d’événement (le cas échéant) à définir lorsque l’achèvement se produit. La structure **WSAOVERLAPPED** peut être utilisée par le fournisseur de services comme un emplacement pour stocker un handle vers les résultats (par exemple, le nombre d’octets transférés, les indicateurs mis à jour, les codes d’erreur, etc.) pour une opération Overlapped particulière. Pour obtenir ces résultats, les clients doivent appeler [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), en passant un pointeur vers la structure OVERLAPPED correspondante.

Si l’indication de saisie semi-automatique basée sur les événements est sélectionnée pour une requête d’e/s avec chevauchement particulière, la routine [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) peut elle-même être utilisée par les clients pour interroger ou attendre la fin de l’opération Overlapped. Si la saisie semi-automatique est sélectionnée pour une requête d’e/s avec chevauchement particulière, seule l’option d’interrogation de **WSPGetOverlappedResult** est disponible. Un client peut également utiliser d’autres moyens d’attendre (comme l’utilisation de [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)) jusqu’à ce que l’objet d’événement correspondant soit signalé ou que la routine de saisie semi-automatique spécifiée ait été appelée par le fournisseur de services. Une fois la saisie semi-automatique indiquée, le client peut appeler **WSPGetOverlappedResult**, dans l’attente que l’appel se termine immédiatement.

## <a name="invoking-socket-io-completion-routines"></a>Appel des routines de fin d’exécution d’e/s de socket

Si le paramètre *lpCompletionRoutine* d’une opération avec chevauchement n’a pas la **valeur null**, il incombe au fournisseur de services d’organiser l’appel de la routine de saisie semi-automatique spécifiée par le client lorsque l’opération avec chevauchement se termine. Étant donné que la routine de saisie semi-automatique doit être exécutée dans le contexte du thread qui a initié l’opération Overlapped, elle ne peut pas être appelée directement à partir du fournisseur de services. Le \_32.DLL Ws2 offre un mécanisme d’appel de procédure asynchrone (APC) pour faciliter l’appel des routines de saisie semi-automatique.

Un fournisseur de services s’arrange pour qu’une fonction soit exécutée dans le thread approprié en appelant [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Cette fonction peut être appelée à partir de n’importe quel processus et contexte de thread, même un contexte différent du thread et du processus qui a été utilisé pour initier l’opération avec chevauchement.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) prend comme paramètres d’entrée un pointeur vers une structure [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) , un pointeur vers une fonction APC à appeler et une valeur de contexte 32 bits qui est ensuite transmise à la fonction APC. Les fournisseurs de services sont toujours fournis avec un pointeur vers la structure **WSATHREADID** appropriée via le paramètre *lpThreadId* de la fonction Overlapped. Le fournisseur doit stocker la structure **WSATHREADID** localement et fournir un pointeur vers cette copie de la structure **WSATHREADID** en tant que paramètre d’entrée à **WPUQueueApc**. Une fois la fonction **WPUQueueApc** retournée, le fournisseur peut supprimer sa copie du **WSATHREADID**.

La procédure [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) met simplement en file d’attente des informations suffisantes pour appeler la fonction APC indiquée avec les paramètres donnés, mais ne l’appelle pas. Lorsque le thread cible entre dans un état d’attente alerté, ces informations sont déplacées dans la file d’attente et un appel est effectué vers la fonction APC dans ce thread cible et le contexte de processus. Étant donné que le mécanisme APC ne prend en charge qu’une seule valeur de contexte 32 bits, la fonction APC ne peut pas être la routine de saisie semi-automatique spécifiée par le client, ce qui implique davantage de paramètres. Le fournisseur de services doit à la place fournir un pointeur vers sa propre fonction APC qui utilise la valeur de contexte fournie pour accéder aux informations de résultat nécessaires à l’opération Overlapped, puis appelle la routine de saisie semi-automatique spécifiée par le client.

Pour les fournisseurs de services dans lesquels un composant en mode utilisateur implémente des e/s avec chevauchement, une utilisation classique du mécanisme APC est la suivante :

-   Lorsque l’opération d’e/s se termine, le fournisseur alloue une petite mémoire tampon et la compresse à l’aide d’un pointeur désignant la procédure de saisie semi-automatique fournie par le client et les valeurs de paramètre à passer à la procédure.
-   Il met en file d’attente un APC, en spécifiant le pointeur vers la mémoire tampon comme valeur de contexte et sa propre procédure intermédiaire comme procédure cible.
-   Lorsque le thread cible entre finalement en état d’attente d’alerte, la procédure intermédiaire du fournisseur de services est appelée dans le contexte de thread approprié.
-   La procédure intermédiaire décompresse simplement les paramètres, libère la mémoire tampon et appelle la procédure de saisie semi-automatique fournie par le client.
-   Pour les fournisseurs de services dans lesquels un composant en mode noyau implémente des e/s avec chevauchement, une implémentation classique est similaire, à ceci près que l’implémentation utilise des interfaces de noyau standard pour mettre l’APC en file d’attente.

la Description des interfaces de noyau appropriées est en dehors de l’étendue de la spécification Windows sockets 2.

> [!Note]  
> les fournisseurs de services doivent autoriser Windows clients sockets 2 à appeler des opérations d’envoi et de réception à partir du contexte de la routine d’exécution d’e/s de socket et à garantir que, pour un socket donné, les routines d’exécution d’e/s ne sont pas imbriquées.

 

Dans certains cas, un fournisseur de services en couche peut avoir besoin de lancer et d’effectuer des opérations avec chevauchement à partir d’un thread de travail interne. Dans ce cas, un [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) n’est pas disponible à partir d’un appel de fonction entrant. L’interface du fournisseur de services fournit un appel de [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)pour obtenir un **WSATHREADID** pour le thread actuel. Quand ce **WSATHREADID** n’est plus nécessaire, ses ressources doivent être retournées en appelant [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread).

 

 
