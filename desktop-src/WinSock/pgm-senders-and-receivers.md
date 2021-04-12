---
description: L’établissement d’une session PGM est semblable à la routine d’établissement de connexion associée à une session TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Expéditeurs et destinataires PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526121"
---
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="f2a9b-103">Expéditeurs et destinataires PGM</span><span class="sxs-lookup"><span data-stu-id="f2a9b-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="f2a9b-104">L’établissement d’une session PGM est semblable à la routine d’établissement de connexion associée à une session TCP.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="f2a9b-105">La sortie significative d’une session TCP, toutefois, est que la sémantique du client et du serveur est inversée. le serveur (expéditeur PGM) se connecte à un groupe de multidiffusion, tandis que le client (récepteur PGM) attend d’accepter une connexion.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="f2a9b-106">Les paragraphes suivants détaillent les étapes de programmation nécessaires à la création d’un expéditeur PGM et d’un récepteur PGM.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="f2a9b-107">Cette page décrit également les modes de données disponibles pour les sessions PGM.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="f2a9b-108">Expéditeur PGM</span><span class="sxs-lookup"><span data-stu-id="f2a9b-108">PGM Sender</span></span>

<span data-ttu-id="f2a9b-109">**Pour créer un expéditeur PGM, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="f2a9b-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="f2a9b-110">Créez un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="f2a9b-111">[**liez**](/windows/desktop/api/winsock/nf-winsock-bind) le socket à inaddr \_ Any.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="f2a9b-112">[**Connectez-vous**](/windows/desktop/api/Winsock2/nf-winsock2-connect) à l’adresse de transmission du groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="f2a9b-113">Aucune négociation de session formelle n’est effectuée avec les clients.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="f2a9b-114">Le processus de connexion est similaire à une [**connexion UDP,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)car il associe une adresse de point de terminaison (le groupe de multidiffusion) au socket.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="f2a9b-115">Une fois terminé, les données peuvent être envoyées sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="f2a9b-116">Lorsqu’un expéditeur crée un socket PGM et le connecte à une adresse de multidiffusion, une session PGM est créée.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="f2a9b-117">Une session de multidiffusion fiable est définie par une combinaison de l’identificateur global unique (GUID) et du port source.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="f2a9b-118">Le GUID est généré par le transport.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="f2a9b-119">Le port sSource est spécifié par le transport, et aucun contrôle n’est fourni sur le port source utilisé.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="f2a9b-120">La réception de données sur un socket d’expéditeur n’est pas autorisée et génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="f2a9b-121">L’extrait de code suivant illustre la configuration d’un expéditeur PGM :</span><span class="sxs-lookup"><span data-stu-id="f2a9b-121">The following code snippet illustrates setting up a PGM sender:</span></span>


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a><span data-ttu-id="f2a9b-122">Récepteur PGM</span><span class="sxs-lookup"><span data-stu-id="f2a9b-122">PGM Receiver</span></span>

<span data-ttu-id="f2a9b-123">**Pour créer un récepteur PGM, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="f2a9b-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="f2a9b-124">Créez un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="f2a9b-125">[**liez**](/windows/desktop/api/winsock/nf-winsock-bind) le socket à l’adresse du groupe de multidiffusion sur lequel l’expéditeur transmet.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="f2a9b-126">Appelez la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) sur le socket pour mettre le socket en mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="f2a9b-127">La fonction listen retourne lorsqu’une session PGM est détectée sur le port et l’adresse du groupe de multidiffusion spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="f2a9b-128">Appelez la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) pour obtenir un nouveau handle de socket correspondant à la session.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="f2a9b-129">Seules les données PGM d’origine (ODATA) déclenchent l’acceptation d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="f2a9b-130">Par conséquent, d’autres trafics PGM (tels que les paquets SPM ou RDATA) peuvent être reçus par le transport, mais n’entraînent pas le retour de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="f2a9b-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="f2a9b-131">Une fois qu’une session est acceptée, le descripteur de socket retourné est utilisé pour la réception de données.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="f2a9b-132">L’envoi de données sur un socket de réception n’est pas autorisé et génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="f2a9b-133">L’extrait de code suivant illustre la configuration d’un récepteur PGM :</span><span class="sxs-lookup"><span data-stu-id="f2a9b-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a><span data-ttu-id="f2a9b-134">Modes de données</span><span class="sxs-lookup"><span data-stu-id="f2a9b-134">Data Modes</span></span>

<span data-ttu-id="f2a9b-135">Les sessions PGM ont deux options pour les modes de données : le mode de message et le mode de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="f2a9b-136">Le mode message est approprié pour les applications qui doivent envoyer des messages discrets, et est spécifié par un type de socket \_ RDM.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="f2a9b-137">Le mode de flux est approprié pour les applications qui doivent envoyer des données de diffusion en continu à des destinataires, tels que des applications vidéo ou vocales, et est spécifié par un type de socket de flux de chaussette \_ .</span><span class="sxs-lookup"><span data-stu-id="f2a9b-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="f2a9b-138">Choix des effets du mode de traitement des données par Winsock.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="f2a9b-139">Prenons l’exemple suivant : un expéditeur PGM en mode message effectue trois appels à la fonction [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , chacun avec une mémoire tampon de 100 octets.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="f2a9b-140">Cette opération apparaît sur le câble sous forme de trois paquets PGM discrets.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="f2a9b-141">Du côté du récepteur, chaque appel à la fonction [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) retourne uniquement 100 octets, même si un tampon de réception plus grand est fourni.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="f2a9b-142">En revanche, avec un expéditeur PGM en mode flux, ces transmissions de 3 100 octets peuvent être fusionnées en moins de trois paquets physiques sur le réseau (ou fusionnés en un seul objet blob de données côté récepteur).</span><span class="sxs-lookup"><span data-stu-id="f2a9b-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="f2a9b-143">Ainsi, lorsque le récepteur appelle l’une des fonctions de réception de Windows Sockets, toute quantité de données reçues par le transport PGM peut être retournée à l’application sans tenir compte de la façon dont les données ont été physiquement transmises ou reçues.</span><span class="sxs-lookup"><span data-stu-id="f2a9b-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



