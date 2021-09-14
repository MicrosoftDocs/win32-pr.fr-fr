---
description: L’envoi et la réception de données PGM sont similaires à l’envoi ou à la réception de données sur n’importe quel Socket. Il existe des considérations spécifiques au PGM, présentées dans les paragraphes suivants.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Envoi et réception de données PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118517"
---
# <a name="sending-and-receiving-pgm-data"></a>Envoi et réception de données PGM

L’envoi et la réception de données PGM sont similaires à l’envoi ou à la réception de données sur n’importe quel Socket. Il existe des considérations spécifiques au PGM, présentées dans les paragraphes suivants.

## <a name="sending-pgm-data"></a>Envoi de données PGM

une fois la session de l’expéditeur PGM créée, les données sont envoyées à l’aide des différentes fonctions d’envoi de Windows sockets : [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)et [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). étant donné que les handles de Windows sockets sont des handles de système de fichiers, d’autres fonctions telles que les fonctions [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) et CRT peuvent également transmettre des données. L’extrait de code suivant illustre une opération d’expéditeur PGM :


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



Lors de l’utilisation du mode message ( \_ la chaussette RDM), chaque appel à une fonction Send se traduit par un message discret, ce qui n’est pas toujours souhaitable. une application peut souhaiter envoyer un message de 2 mégaoctets avec plusieurs appels à [**Envoyer**](/windows/desktop/api/Winsock2/nf-winsock2-send). Dans ce cas, l’expéditeur peut définir l’option [RM \_ Set \_ message \_ Boundary](socket-options.md) Socket pour indiquer la taille du message qui suit.

Si la fenêtre d’envoi est pleine, un nouvel envoi à partir de l’application n’est pas accepté tant que la fenêtre n’a pas été avancée. La tentative d’envoi sur un socket non bloquant échoue avec WSAEWOULDBLOCK ; un socket bloquant se bloque simplement jusqu’à ce que la fenêtre avance jusqu’au point où les données demandées peuvent être mises en mémoire tampon et envoyées. Dans les e/s avec chevauchement, l’opération ne se termine pas tant que la fenêtre n’a pas suffisamment d’avance pour accueillir les nouvelles données.

## <a name="receiving-pgm-data"></a>Réception de données PGM

une fois qu’une session de récepteur PGM est créée, les données sont reçues à l’aide des différentes fonctions de réception de Windows sockets : [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)et [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom). étant donné que les handles de Windows sockets sont également des descripteurs de fichiers, les fonctions [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) et CRT peuvent également être utilisées pour recevoir les données de session PGM. Le transport transfère les données jusqu’au destinataire lorsqu’elles arrivent tant que les données sont dans l’ordre. Le transport garantit que les données retournées sont contiguës et exemptes de doublons. L’extrait de code suivant illustre une opération de réception PGM :


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



Lors de l’utilisation du mode message (RDM de chaussette \_ ), le transport indique quand un message partiel est reçu, avec l’erreur WSAEMSGSIZE ou en définissant l' \_ indicateur partiel MSG au retour des fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) et [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) . Lorsque le dernier fragment de la totalité du message est retourné au client, l’erreur ou l’indicateur n’est pas indiqué.

Lorsque la session est terminée correctement, l’opération de réception échoue avec WSAEDISCON. En cas de perte de données dans le transport, le protocole PGM met temporairement en mémoire tampon les paquets hors séquence et tente de récupérer les données perdues. Si la perte de données ne peut pas être récupérée, l’opération de réception échoue avec WSAECONNRESET et la session est arrêtée. La session peut être réinitialisée en raison de diverses conditions, y compris les suivantes :

-   Le récepteur ou la vitesse de connexion entrante est trop lent pour suivre le rythme du débit des données entrantes.
-   Une perte excessive de données se produit, peut-être en raison de conditions réseau temporaires, telles que les problèmes de routage, l’instabilité du réseau, etc.
-   Une erreur irrécupérable s’est produite sur l’expéditeur.
-   Une utilisation excessive des ressources se produit sur l’ordinateur local, par exemple le dépassement du stockage de tampons interne maximal autorisé ou la présence d’une condition de ressources insuffisantes.
-   Une erreur de vérification de cohérence des données se produit.
-   l’échec d’un composant PGM dépend de, tels que TCP/IP ou Windows sockets.

Le premier et le deuxième élément de la liste ci-dessus peuvent entraîner une mise en mémoire tampon excessive du récepteur avant de manquer de ressources, ou avant de se déplacer au-delà de la fenêtre de l’expéditeur.

## <a name="terminating-a-pgm-session"></a>Fin d’une session PGM

L’expéditeur ou le récepteur PGM peut arrêter d’envoyer ou de recevoir des données en appelant [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). Le récepteur doit appeler **opération closesocket** sur les sockets d’écoute et de réception pour empêcher les fuites de handle. L’appel de [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) sur l’expéditeur avant l’appel de **opération closesocket** garantit que toutes les données sont envoyées et garantit que les données de réparation sont conservées jusqu’à ce que la fenêtre d’envoi avance jusqu’à la dernière séquence de données, même si l’application elle-même se termine.

 

 
