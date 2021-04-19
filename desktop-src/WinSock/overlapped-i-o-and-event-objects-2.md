---
description: Windows Sockets 2 prend en charge les e/s avec chevauchement et tous les fournisseurs de transport prennent en charge cette fonctionnalité.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Objets d’e/s et d’événement avec chevauchement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513220"
---
# <a name="overlapped-io-and-event-objects"></a>Objets d’e/s et d’événement avec chevauchement

Windows Sockets 2 prend en charge les e/s avec chevauchement et tous les fournisseurs de transport prennent en charge cette fonctionnalité. Les e/s avec chevauchement suivent le modèle établi dans Windows et peuvent être exécutées sur les sockets créés avec la fonction de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou les sockets créés avec la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) avec l’indicateur de **\_ \_ chevauchement d’indicateur WSA** défini dans le paramètre *dwFlags* .

> [!Note]  
> La création d’un socket avec l’attribut Overlapped n’a aucun impact sur le fait qu’un socket est actuellement en mode blocage ou non bloquant. Les sockets créés avec l’attribut Overlapped peuvent être utilisés pour effectuer des e/s avec chevauchement, ce qui ne modifie pas le mode de blocage d’un Socket. Étant donné que les opérations d’e/s avec chevauchement ne sont pas bloquées, le mode de blocage d’un socket n’est pas pertinent pour ces opérations.

 

Pour la réception, les applications utilisent les fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) pour fournir des mémoires tampons dans lesquelles les données doivent être reçues. Si une ou plusieurs mémoires tampons sont publiées avant le moment où les données ont été reçues par le réseau, ces données peuvent être placées dans les tampons de l’utilisateur dès qu’elles arrivent. Ainsi, il peut éviter l’opération de copie qui, autrement, se produirait au moment de l’appel de la fonction [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) ou [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) . Si des données sont déjà présentes lors de la publication des tampons de réception, elles sont copiées immédiatement dans les tampons de l’utilisateur.

Si des données arrivent quand aucune mémoire tampon de réception n’a été publiée par l’application, le réseau passe au style de fonctionnement synchrone familier. Autrement dit, les données entrantes sont mises en mémoire tampon jusqu’à ce que l’application envoie un appel de réception et fournit ainsi une mémoire tampon dans laquelle les données peuvent être copiées. Une exception est quand l’application utilise [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir la taille de la mémoire tampon de réception sur zéro. Dans ce cas, les protocoles Reliable autorisent uniquement la réception des données lorsque les tampons d’application ont été publiés et la perte des données sur les protocoles non fiables.

Du côté de l’envoi, les applications utilisent [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) pour fournir des pointeurs aux mémoires tampons remplies, puis décident de ne pas perturber les tampons jusqu’à ce que le réseau ait consommé le contenu de la mémoire tampon.

Les appels d’envoi et de réception superposés sont retournés immédiatement. Une valeur de retour égale à zéro indique que l’opération d’e/s a été effectuée immédiatement et que l’indication d’achèvement correspondante a déjà eu lieu. Autrement dit, l’objet événement associé a été signalé, ou une routine de saisie semi-automatique a été mise en file d’attente et sera exécutée lorsque le thread appelant passera à l’état d’attente de l’alerte.

Une valeur de retour de \_ l’erreur de socket couplée avec un code d’erreur d' [ \_ e/s de WSA \_ en attente](windows-sockets-error-codes-2.md) indique que l’opération avec chevauchement a été lancée avec succès et qu’une indication suivante sera fournie quand les mémoires tampons d’envoi ont été consommées ou lorsqu’une opération de réception a été effectuée. Toutefois, pour les sockets qui sont du style de flux d’octets, l’indication de saisie semi-automatique se produit chaque fois que les données entrantes sont épuisées, que les mémoires tampons soient pleines ou non. Tout autre code d’erreur indique que l’opération avec chevauchement n’a pas été lancée avec succès et qu’aucune indication d’achèvement n’est à venir.

Les opérations d’envoi et de réception peuvent être superposées. Les fonctions Receive peuvent être appelées plusieurs fois pour poster des tampons de réception en vue de la préparation des données entrantes, et les fonctions Send peuvent être appelées plusieurs fois pour mettre en file d’attente plusieurs mémoires tampons à envoyer. Alors que l’application peut reposer sur une série de mémoires tampons d’envoi avec chevauchement envoyées dans l’ordre indiqué, les indications d’achèvement correspondantes peuvent se produire dans un ordre différent. De même, du côté de la réception, les tampons peuvent être remplis dans l’ordre dans lequel ils sont fournis, mais les indications de saisie semi-automatique peuvent se produire dans un ordre différent.

Dans de nombreux cas, les opérations de chevauchement Winsock utilisant [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)et des fonctions similaires peuvent être annulées. Toutefois, le comportement n’est pas défini pour l’utilisation continue d’un socket qui a annulé des opérations en suspens. La fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) doit être appelée après l’annulation d’une opération avec chevauchement. Par conséquent, pour des résultats optimaux, au lieu d’annuler directement les e/s, la fonction **opération closesocket** doit être appelée pour fermer le socket qui finit par cesser toutes les opérations en attente.

La fonctionnalité d’achèvement différé des e/s avec chevauchement est également disponible pour [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), qui est une version améliorée de [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
