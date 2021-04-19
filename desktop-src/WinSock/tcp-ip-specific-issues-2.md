---
description: Certaines techniques de programmation s’exécutent dans des problèmes de performances liés à l’implémentation de TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problèmes spécifiques à TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518307"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="2384b-103">Problèmes spécifiques à TCP/IP</span><span class="sxs-lookup"><span data-stu-id="2384b-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="2384b-104">Certaines techniques de programmation s’exécutent dans des problèmes de performances liés à l’implémentation de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2384b-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="2384b-105">De tels problèmes de performances ne suggèrent pas que le protocole TCP/IP est inefficace ou un goulot d’étranglement des performances. au lieu de cela, ces problèmes sont observés lorsque les opérations TCP/IP ne sont pas comprises.</span><span class="sxs-lookup"><span data-stu-id="2384b-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="2384b-106">Les problèmes suivants identifient les scénarios courants dans lesquels la combinaison des choix d’opérations TCP/IP et de développement d’applications réseau entraîne une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="2384b-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="2384b-107">Connectez-vous à des applications lourdes.</span><span class="sxs-lookup"><span data-stu-id="2384b-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="2384b-108">Certaines applications instancient une nouvelle connexion TCP pour chaque transaction.</span><span class="sxs-lookup"><span data-stu-id="2384b-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="2384b-109">L’établissement de connexions TCP prend du temps, fournit des RTTs supplémentaires et est soumis à un démarrage lent.</span><span class="sxs-lookup"><span data-stu-id="2384b-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="2384b-110">En outre, les connexions fermées sont soumises à TIME-WAIT, qui consomme des ressources système.</span><span class="sxs-lookup"><span data-stu-id="2384b-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="2384b-111">Les applications à connexion intensive sont courantes, car elles sont faciles à créer. le test et la gestion des erreurs sont très simples.</span><span class="sxs-lookup"><span data-stu-id="2384b-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="2384b-112">La détection des erreurs sur une connexion permanente peut nécessiter du code et des efforts considérables, et par conséquent, elle n’est parfois pas terminée.</span><span class="sxs-lookup"><span data-stu-id="2384b-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="2384b-113">Résolvez cette situation en réutilisant la connexion TCP.</span><span class="sxs-lookup"><span data-stu-id="2384b-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="2384b-114">Cela peut entraîner une sérialisation sur la connexion TCP, sauf si les transactions sont multiplexées sur plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="2384b-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="2384b-115">Si cette approche est prise, le nombre de connexions doit être limité à deux, et l’encadrement de la couche application et la gestion avancée des erreurs sont requis.</span><span class="sxs-lookup"><span data-stu-id="2384b-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="2384b-116">Mémoires tampons d’envoi de longueur nulle et blocages envoyés.</span><span class="sxs-lookup"><span data-stu-id="2384b-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="2384b-117">La désactivation de la mise en mémoire tampon à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir la mémoire tampon d’envoi ( \_ SNDBUF) sur zéro est semblable à la désactivation de la mise en cache du disque.</span><span class="sxs-lookup"><span data-stu-id="2384b-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="2384b-118">Lors de la définition de la mémoire tampon d’envoi à zéro et de l’émission d’envois de blocage, une application a une chance de 50% d’atteindre un accusé de réception retardé de 200 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2384b-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="2384b-119">Ne désactivez pas la mise en mémoire tampon d’envoi, sauf si vous avez pris en compte l’impact sur tous les environnements réseau.</span><span class="sxs-lookup"><span data-stu-id="2384b-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="2384b-120">Une exception : les données de streaming utilisant des e/s avec chevauchement doivent définir la mémoire tampon d’envoi sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2384b-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="2384b-121">Modèle de programmation Send-Send-Receive.</span><span class="sxs-lookup"><span data-stu-id="2384b-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="2384b-122">La structuration d’une application pour exécuter send-send-receives augmente vos chances de rencontrer l’algorithme Nagle, ce qui entraîne un délai de RTT + 200 ms.</span><span class="sxs-lookup"><span data-stu-id="2384b-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="2384b-123">L’algorithme Nagle peut être rencontré si le dernier envoi est inférieur à la taille maximale du segment TCP (MSS, le nombre maximal de données dans un seul datagramme).</span><span class="sxs-lookup"><span data-stu-id="2384b-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="2384b-124">MSS peut être une valeur très élevée (64 Ko dans IPv4, et même plus grand dans IPv6). par conséquent, ne comptez pas sur un MSS généralement de petite taille.</span><span class="sxs-lookup"><span data-stu-id="2384b-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="2384b-125">Une meilleure option consiste à combiner les deux envois en une seule envoi à l’aide de la fonction [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou **memcpy** .</span><span class="sxs-lookup"><span data-stu-id="2384b-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="2384b-126">Un grand nombre de connexions simultanées.</span><span class="sxs-lookup"><span data-stu-id="2384b-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="2384b-127">Les connexions simultanées ne doivent pas dépasser deux, sauf dans les applications à usage spécial.</span><span class="sxs-lookup"><span data-stu-id="2384b-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="2384b-128">Le dépassement de deux connexions simultanées entraîne l’ingaspillage des ressources.</span><span class="sxs-lookup"><span data-stu-id="2384b-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="2384b-129">Une bonne règle consiste à avoir jusqu’à quatre connexions à courte durée de vie, ou deux connexions persistantes par destination.</span><span class="sxs-lookup"><span data-stu-id="2384b-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2384b-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2384b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2384b-131">Comportement de l’application</span><span class="sxs-lookup"><span data-stu-id="2384b-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="2384b-132">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="2384b-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="2384b-133">L’algorithme Nagle</span><span class="sxs-lookup"><span data-stu-id="2384b-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



