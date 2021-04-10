---
description: L’envoi et la réception de données PGM sont similaires à l’envoi ou à la réception de données sur n’importe quel Socket. Il existe des considérations spécifiques au PGM, présentées dans les paragraphes suivants.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Envoi et réception de données PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115051"
---
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="52235-104">Envoi et réception de données PGM</span><span class="sxs-lookup"><span data-stu-id="52235-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="52235-105">L’envoi et la réception de données PGM sont similaires à l’envoi ou à la réception de données sur n’importe quel Socket.</span><span class="sxs-lookup"><span data-stu-id="52235-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="52235-106">Il existe des considérations spécifiques au PGM, présentées dans les paragraphes suivants.</span><span class="sxs-lookup"><span data-stu-id="52235-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="52235-107">Envoi de données PGM</span><span class="sxs-lookup"><span data-stu-id="52235-107">Sending PGM Data</span></span>

<span data-ttu-id="52235-108">Une fois la session de l’expéditeur PGM créée, les données sont envoyées à l’aide des différentes fonctions Send de Windows Sockets : [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)et [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="52235-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="52235-109">Étant donné que les handles Windows Sockets sont des handles de système de fichiers, d’autres fonctions telles que les fonctions [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) et CRT peuvent également transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="52235-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="52235-110">L’extrait de code suivant illustre une opération d’expéditeur PGM :</span><span class="sxs-lookup"><span data-stu-id="52235-110">The following code snippet illustrates a PGM sender operation:</span></span>


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



<span data-ttu-id="52235-111">Lors de l’utilisation du mode message ( \_ la chaussette RDM), chaque appel à une fonction Send se traduit par un message discret, ce qui n’est pas toujours souhaitable. une application peut souhaiter envoyer un message de 2 mégaoctets avec plusieurs appels à [**Envoyer**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span><span class="sxs-lookup"><span data-stu-id="52235-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="52235-112">Dans ce cas, l’expéditeur peut définir l’option [RM \_ Set \_ message \_ Boundary](socket-options.md) Socket pour indiquer la taille du message qui suit.</span><span class="sxs-lookup"><span data-stu-id="52235-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="52235-113">Si la fenêtre d’envoi est pleine, un nouvel envoi à partir de l’application n’est pas accepté tant que la fenêtre n’a pas été avancée.</span><span class="sxs-lookup"><span data-stu-id="52235-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="52235-114">La tentative d’envoi sur un socket non bloquant échoue avec WSAEWOULDBLOCK ; un socket bloquant se bloque simplement jusqu’à ce que la fenêtre avance jusqu’au point où les données demandées peuvent être mises en mémoire tampon et envoyées.</span><span class="sxs-lookup"><span data-stu-id="52235-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="52235-115">Dans les e/s avec chevauchement, l’opération ne se termine pas tant que la fenêtre n’a pas suffisamment d’avance pour accueillir les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="52235-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="52235-116">Réception de données PGM</span><span class="sxs-lookup"><span data-stu-id="52235-116">Receiving PGM Data</span></span>

<span data-ttu-id="52235-117">Une fois qu’une session de récepteur PGM est créée, les données sont reçues à l’aide des différentes fonctions de réception de Windows Sockets : [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)et [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="52235-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="52235-118">Étant donné que les handles Windows Sockets sont également des descripteurs de fichiers, les fonctions [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) et CRT peuvent également être utilisées pour recevoir les données de session PGM.</span><span class="sxs-lookup"><span data-stu-id="52235-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="52235-119">Le transport transfère les données jusqu’au destinataire lorsqu’elles arrivent tant que les données sont dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="52235-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="52235-120">Le transport garantit que les données retournées sont contiguës et exemptes de doublons.</span><span class="sxs-lookup"><span data-stu-id="52235-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="52235-121">L’extrait de code suivant illustre une opération de réception PGM :</span><span class="sxs-lookup"><span data-stu-id="52235-121">The following code snippet illustrates a PGM receive operation:</span></span>


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



<span data-ttu-id="52235-122">Lors de l’utilisation du mode message (RDM de chaussette \_ ), le transport indique quand un message partiel est reçu, avec l’erreur WSAEMSGSIZE ou en définissant l' \_ indicateur partiel MSG au retour des fonctions [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) et [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="52235-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="52235-123">Lorsque le dernier fragment de la totalité du message est retourné au client, l’erreur ou l’indicateur n’est pas indiqué.</span><span class="sxs-lookup"><span data-stu-id="52235-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="52235-124">Lorsque la session est terminée correctement, l’opération de réception échoue avec WSAEDISCON.</span><span class="sxs-lookup"><span data-stu-id="52235-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="52235-125">En cas de perte de données dans le transport, le protocole PGM met temporairement en mémoire tampon les paquets hors séquence et tente de récupérer les données perdues.</span><span class="sxs-lookup"><span data-stu-id="52235-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="52235-126">Si la perte de données ne peut pas être récupérée, l’opération de réception échoue avec WSAECONNRESET et la session est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="52235-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="52235-127">La session peut être réinitialisée en raison de diverses conditions, y compris les suivantes :</span><span class="sxs-lookup"><span data-stu-id="52235-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="52235-128">Le récepteur ou la vitesse de connexion entrante est trop lent pour suivre le rythme du débit des données entrantes.</span><span class="sxs-lookup"><span data-stu-id="52235-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="52235-129">Une perte excessive de données se produit, peut-être en raison de conditions réseau temporaires, telles que les problèmes de routage, l’instabilité du réseau, etc.</span><span class="sxs-lookup"><span data-stu-id="52235-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="52235-130">Une erreur irrécupérable s’est produite sur l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="52235-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="52235-131">Une utilisation excessive des ressources se produit sur l’ordinateur local, par exemple le dépassement du stockage de tampons interne maximal autorisé ou la présence d’une condition de ressources insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="52235-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="52235-132">Une erreur de vérification de cohérence des données se produit.</span><span class="sxs-lookup"><span data-stu-id="52235-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="52235-133">L’échec d’un composant PGM dépend de, tels que TCP/IP ou Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="52235-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="52235-134">Le premier et le deuxième élément de la liste ci-dessus peuvent entraîner une mise en mémoire tampon excessive du récepteur avant de manquer de ressources, ou avant de se déplacer au-delà de la fenêtre de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="52235-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="52235-135">Fin d’une session PGM</span><span class="sxs-lookup"><span data-stu-id="52235-135">Terminating A PGM Session</span></span>

<span data-ttu-id="52235-136">L’expéditeur ou le récepteur PGM peut arrêter d’envoyer ou de recevoir des données en appelant [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span><span class="sxs-lookup"><span data-stu-id="52235-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="52235-137">Le récepteur doit appeler **opération closesocket** sur les sockets d’écoute et de réception pour empêcher les fuites de handle.</span><span class="sxs-lookup"><span data-stu-id="52235-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="52235-138">L’appel de [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) sur l’expéditeur avant l’appel de **opération closesocket** garantit que toutes les données sont envoyées et garantit que les données de réparation sont conservées jusqu’à ce que la fenêtre d’envoi avance jusqu’à la dernière séquence de données, même si l’application elle-même se termine.</span><span class="sxs-lookup"><span data-stu-id="52235-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
