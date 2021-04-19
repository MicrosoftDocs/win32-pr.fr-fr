---
description: Ce guide identifie une application lente en tant qu’application Microsoft Windows avec des performances altérées.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconnaître les applications lentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534715"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="ce4ac-103">Reconnaître les applications lentes</span><span class="sxs-lookup"><span data-stu-id="ce4ac-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="ce4ac-104">Ce guide identifie une application *lente* en tant qu’application Microsoft Windows avec des performances altérées.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="ce4ac-105">Une application lente présente un ou plusieurs des symptômes suivants :</span><span class="sxs-lookup"><span data-stu-id="ce4ac-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="ce4ac-106">L’utilisation du processeur et du réseau est faible.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="ce4ac-107">L’ordinateur semble être en attente d’un événement.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="ce4ac-108">Souvent, l’application est en attente sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="ce4ac-109">La désactivation de l’algorithme Nagle par le biais de l' \_ option de socket TCP NoDelay augmente les performances.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="ce4ac-110">Cela indique d’autres problèmes et ne doit pas être considéré comme une solution.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="ce4ac-111">La désactivation de l’algorithme Nagle augmente la surcharge du protocole.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="ce4ac-112">N’utilisez pas cette méthode comme correctif pour les applications endommagées, mais uniquement en tant qu’indication, l’application a besoin d’autres tâches pour résoudre les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="ce4ac-113">L’application présente une surcharge élevée.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="ce4ac-114">Pour calculer la charge de votre application, déterminez la quantité de données que vous souhaitez transférer dans chaque direction.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="ce4ac-115">Utilisez ensuite netstat et ajoutez (pour Ethernet) 60 octets pour chaque paquet et 500 octets pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="ce4ac-116">La meilleure surcharge qui peut être attendue pour la diffusion sur Ethernet est d’environ 6%.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="ce4ac-117">Pour une connexion par modem, la meilleure surcharge est d’environ 2%, en raison du fait qu’une liaison PPP utilise la compression d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="ce4ac-118">Pour plus d’informations, consultez calcul de la [surcharge avec netstat](calculating-overhead-with-netstat-2.md) .</span><span class="sxs-lookup"><span data-stu-id="ce4ac-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="ce4ac-119">La réponse de l’application est lente lorsque la connexion a un temps RTT important.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="ce4ac-120">En supposant que l’application n’approche pas de la bande passante de la liaison, un RTT important doit avoir peu ou pas d’effet.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="ce4ac-121">Un ralentissement spectaculaire d’un RTT important est un signe clair de traitement sérialisé et de nombreuses petites transactions.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="ce4ac-122">Chaque application doit être testée dans un environnement avec un temps RTT important.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="ce4ac-123">Cela révèle la plupart des applications qui subissent des choix de développement médiocres.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="ce4ac-124">Ce test peut être effectué dans plusieurs environnements, y compris un réseau local sans fil, un simulateur de délai de liaison ou un réseau satellite.</span><span class="sxs-lookup"><span data-stu-id="ce4ac-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce4ac-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce4ac-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce4ac-126">Comportement de l’application</span><span class="sxs-lookup"><span data-stu-id="ce4ac-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="ce4ac-127">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="ce4ac-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ce4ac-128">L’algorithme Nagle</span><span class="sxs-lookup"><span data-stu-id="ce4ac-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



