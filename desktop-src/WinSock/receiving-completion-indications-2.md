---
description: 'Plusieurs options sont disponibles pour recevoir des indications de saisie semi-automatique, fournissant ainsi aux applications des niveaux de flexibilité appropriés. Celles-ci incluent : en attente (ou blocage) sur les objets d’événement, les objets d’événement d’interrogation et les routines d’exécution d’e/s de Socket.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Réception des indications d’achèvement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd05d8297af17c26393b5db113fac283b39fcbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534068"
---
# <a name="receiving-completion-indications"></a>Réception des indications d’achèvement

Plusieurs options sont disponibles pour recevoir des indications de saisie semi-automatique, fournissant ainsi aux applications des niveaux de flexibilité appropriés. Celles-ci incluent : en attente (ou blocage) sur les objets d’événement, les objets d’événement d’interrogation et les routines d’exécution d’e/s de Socket.

## <a name="blocking-and-waiting-for-completion-indication"></a>Blocage et attente de l’indication d’achèvement

Les applications peuvent bloquer en attendant qu’un ou plusieurs objets d’événement soient définis à l’aide de la fonction [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . Dans les implémentations de Windows, le processus ou le thread se bloque véritablement. Étant donné que les objets d’événement Windows Sockets 2 sont implémentés en tant qu’événements Windows, la fonction Windows native, [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) peut également être utilisée à cet effet. Cela s’avère particulièrement utile si le thread doit attendre les événements socket et non Socket.

## <a name="polling-for-completion-indication"></a>Interrogation de l’indication d’achèvement

Les applications qui préfèrent ne pas bloquer peuvent utiliser la fonction [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) pour interroger l’état d’achèvement associé à un objet d’événement particulier. Cette fonction indique si l’opération Overlapped est terminée et, si elle est terminée, organise la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) pour récupérer l’état d’erreur de l’opération Overlapped.

## <a name="using-socket-io-completion-routines"></a>Utilisation des routines d’exécution d’e/s de socket

Les fonctions utilisées pour initier des e/s avec chevauchement ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) prennent toutes *lpCompletionRoutine* comme paramètre d’entrée facultatif. Il s’agit d’un pointeur vers une fonction spécifique à l’application qui est appelée après l’exécution d’une opération d’e/s avec chevauchement correctement lancée (avec succès ou autre). La routine de saisie semi-automatique suit les mêmes règles que celles stipulées pour les routines d’exécution d’e/s de fichier Windows. Autrement dit, la routine d’achèvement n’est pas appelée tant que le thread n’est pas dans un état d’attente alerté, par exemple lorsque la fonction [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) est appelée avec l' `fAlertable` indicateur défini. Une application qui utilise l’option de routine d’achèvement pour une requête d’e/s avec chevauchement particulière peut ne pas utiliser l’option wait de [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) pour cette même demande d’e/s avec chevauchement.

Les transports permettent à une application d’appeler des opérations d’envoi et de réception à partir du contexte de la routine d’exécution d’e/s de socket et de garantir que, pour un socket donné, les routines d’exécution d’e/s ne sont pas imbriquées. Cela permet de faire en sorte que les transmissions de données sensibles au temps se produisent entièrement dans un contexte préemptif.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Résumé des mécanismes d’indication de fin avec chevauchement

L’indication d’achèvement d’e/s avec chevauchement particulière à utiliser pour une opération Overlapped donnée est déterminée par le fait que l’application fournit un pointeur vers une fonction d’achèvement, si une structure [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) est référencée et par la valeur du membre **hEvent** dans la structure **WSAOVERLAPPED** (si elle est fournie). Le tableau suivant résume la sémantique de saisie semi-automatique pour un socket Overlapped et montre les différentes combinaisons de *lpOverlapped*, **hEvent** et *lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Indication de la saisie semi-automatique                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicable | Ignoré               | L’opération se termine de façon synchrone. Il se comporte comme s’il s’agissait d’un socket nonoverlapped.                                                                                                                                      |
| ! NUL          | NULL           | NULL                  | L’opération se termine, mais il n’existe pas de mécanisme de saisie semi-automatique pris en charge par Windows Sockets 2. Le mécanisme de port de terminaison (s’il est pris en charge) peut être utilisé dans ce cas. Sinon, il n’y a aucune notification de fin d’exécution. |
| ! NUL          | ! NUL          | NULL                  | L’opération termine la superposition, la notification par l’objet d’événement de signalisation.                                                                                                                                                  |
| ! NUL          | Ignoré        | ! NUL                 | L’opération se termine par la routine de fin de la planification.                                                                                                                                           |



 

 

 
