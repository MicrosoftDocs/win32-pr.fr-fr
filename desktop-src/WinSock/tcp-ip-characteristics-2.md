---
description: TCP/IP a des caractéristiques qui permettent au protocole de fonctionner comme des exigences de mise en œuvre standardisées.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Caractéristiques de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865961"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="117da-103">Caractéristiques de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="117da-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="117da-104">TCP/IP a des caractéristiques qui permettent au protocole de fonctionner comme des exigences de mise en œuvre standardisées.</span><span class="sxs-lookup"><span data-stu-id="117da-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="117da-105">Ces caractéristiques peuvent être combinées à des choix de développement qui entraînent des performances médiocres.</span><span class="sxs-lookup"><span data-stu-id="117da-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="117da-106">L’impact de ces caractéristiques TCP/IP sur une application varie selon que l’application est transactionnelle ou de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="117da-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="117da-107">Les applications transactionnelles sont affectées par la surcharge requise pour l’établissement et l’arrêt de la connexion.</span><span class="sxs-lookup"><span data-stu-id="117da-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="117da-108">Par exemple, chaque fois qu’une connexion est établie sur un réseau Ethernet, trois paquets d’environ 60 octets chacun doivent être envoyés, et environ un RTT est requis pour l’échange.</span><span class="sxs-lookup"><span data-stu-id="117da-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="117da-109">Lorsque l’arrêt d’une connexion se produit, quatre paquets sont échangés.</span><span class="sxs-lookup"><span data-stu-id="117da-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="117da-110">C’est le cas pour chaque connexion ; une application qui ouvre et ferme des connexions entraîne souvent cette surcharge sur chaque occurrence.</span><span class="sxs-lookup"><span data-stu-id="117da-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="117da-111">Un autre aspect de TCP/IP est le *démarrage lent*, qui a lieu chaque fois qu’une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="117da-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="117da-112">Le démarrage lent est une limite artificielle sur le nombre de segments de données qui peuvent être envoyés avant la réception de l’accusé de réception de ces segments.</span><span class="sxs-lookup"><span data-stu-id="117da-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="117da-113">Le démarrage lent est conçu pour limiter l’encombrement du réseau.</span><span class="sxs-lookup"><span data-stu-id="117da-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="117da-114">Lorsqu’une connexion sur Ethernet est établie, quelle que soit la taille de la fenêtre du récepteur, une transmission de 4 Ko peut prendre jusqu’à 3-4 de temps RTT en raison d’un démarrage lent.</span><span class="sxs-lookup"><span data-stu-id="117da-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="117da-115">Une optimisation TCP/IP appelée l’algorithme Nagle peut également limiter la vitesse de transfert de données sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="117da-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="117da-116">L’algorithme Nagle est conçu pour réduire la surcharge de protocole pour les applications qui envoient de petites quantités de données, telles que Telnet, qui envoie un caractère unique à la fois.</span><span class="sxs-lookup"><span data-stu-id="117da-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="117da-117">Au lieu d’envoyer immédiatement un paquet avec un grand nombre d’en-têtes et de petites données, la pile attend davantage de données de l’application, ou un accusé de réception, avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="117da-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="117da-118">Les accusés de réception différés, communément appelés *accusés de réception différés*, sont également conçus dans TCP/IP pour permettre une intégration plus efficace des accusés de réception lorsque les données de retour sont à venir de l’application côté réception.</span><span class="sxs-lookup"><span data-stu-id="117da-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="117da-119">Malheureusement, si ces données ne sont pas à venir et que le côté expéditeur attend un accusé de réception, des retards d’environ 200 millisecondes par envoi peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="117da-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="117da-120">Lorsqu’une connexion TCP est fermée, les ressources de connexion au niveau du nœud qui a initié la fermeture sont placées dans un état d’attente, appelé temps-attente, pour assurer la protection contre la corruption des données si des paquets en double restent dans le réseau.</span><span class="sxs-lookup"><span data-stu-id="117da-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="117da-121">Cela permet de s’assurer que les deux extrémités sont terminées avec la connexion.</span><span class="sxs-lookup"><span data-stu-id="117da-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="117da-122">Cela peut entraîner une épuisement des ressources requises par connexion, telles que la RAM et les ports, lorsque les applications ouvrent et ferment fréquemment des connexions.</span><span class="sxs-lookup"><span data-stu-id="117da-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="117da-123">En plus d’être affectées par un accusé de réception retardé et d’autres schémas d’évitement de congestion, les applications de streaming peuvent également être affectées par une taille de fenêtre de réception par défaut trop petite à l’extrémité de réception.</span><span class="sxs-lookup"><span data-stu-id="117da-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="117da-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="117da-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="117da-125">Comportement de l’application</span><span class="sxs-lookup"><span data-stu-id="117da-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="117da-126">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="117da-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="117da-127">L’algorithme Nagle</span><span class="sxs-lookup"><span data-stu-id="117da-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



