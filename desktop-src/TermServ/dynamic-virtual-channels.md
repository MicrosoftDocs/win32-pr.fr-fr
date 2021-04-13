---
title: Canaux virtuels dynamiques
description: Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379897"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="8b47c-103">Canaux virtuels dynamiques</span><span class="sxs-lookup"><span data-stu-id="8b47c-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="8b47c-104">Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC).</span><span class="sxs-lookup"><span data-stu-id="8b47c-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="8b47c-105">Les API DVC répondent à plusieurs limitations qui existaient dans les API SVC entre le client et le serveur, par exemple :</span><span class="sxs-lookup"><span data-stu-id="8b47c-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="8b47c-106">Un nombre limité de canaux</span><span class="sxs-lookup"><span data-stu-id="8b47c-106">A limited number of channels</span></span>
-   <span data-ttu-id="8b47c-107">Reconstruction des paquets</span><span class="sxs-lookup"><span data-stu-id="8b47c-107">Packet reconstruction</span></span>

<span data-ttu-id="8b47c-108">Les API DVC vous aident à implémenter des modules côté serveur et client d’une connexion Services Bureau à distance qui communiquent entre eux.</span><span class="sxs-lookup"><span data-stu-id="8b47c-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="8b47c-109">À l’instar de nombreuses autres architectures client/serveur, une connexion est établie sur la base d’un élément de données communément convenu sous le terme de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8b47c-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="8b47c-110">Un exemple similaire est le protocole TCP/IP, où un point de terminaison est établi via une combinaison d’adresse IP de serveur et de nom de port.</span><span class="sxs-lookup"><span data-stu-id="8b47c-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="8b47c-111">Un autre exemple est canaux nommés, où un point de terminaison est une combinaison du nom du serveur et du nom du canal.</span><span class="sxs-lookup"><span data-stu-id="8b47c-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="8b47c-112">Dans une connexion Services Bureau à distance, il n’y a que deux parties impliquées.</span><span class="sxs-lookup"><span data-stu-id="8b47c-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="8b47c-113">Par conséquent, le point de terminaison se compose d’une simple chaîne arbitraire qui identifie de façon unique la connexion.</span><span class="sxs-lookup"><span data-stu-id="8b47c-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="8b47c-114">À l’instar de TCP/IP et des canaux nommés, plusieurs connexions peuvent démarrer à partir du même nom de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8b47c-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="8b47c-115">Dans ce sens, les connexions n’ont pas de noms ; simplement un écouteur qui attend les demandes entrantes sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8b47c-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="8b47c-116">Les API DVC se composent des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8b47c-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="8b47c-117">API client</span><span class="sxs-lookup"><span data-stu-id="8b47c-117">Client APIs</span></span>

    <span data-ttu-id="8b47c-118">Ces API sont disponibles dans le client Connexion Bureau à distance (RDC) sous la forme d’un plug-in.</span><span class="sxs-lookup"><span data-stu-id="8b47c-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="8b47c-119">Le côté client est en mode passif, où il écoute les connexions entrantes, mais n’établit pas de connexion activement.</span><span class="sxs-lookup"><span data-stu-id="8b47c-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="8b47c-120">API serveur</span><span class="sxs-lookup"><span data-stu-id="8b47c-120">Server APIs</span></span>

    <span data-ttu-id="8b47c-121">Ces API initialisent activement la connexion.</span><span class="sxs-lookup"><span data-stu-id="8b47c-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="8b47c-122">Pour plus d’informations sur l’écriture d’un module de canal virtuel dynamique (DVC), consultez détails de l' [implémentation DVC](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="8b47c-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




