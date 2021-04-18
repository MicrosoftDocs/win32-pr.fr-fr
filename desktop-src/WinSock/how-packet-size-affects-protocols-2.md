---
description: Les problèmes liés à la taille des paquets multimédias décrits dans la rubrique, à propos de la taille des paquets multimédias, affectent différemment les différents \_ protocoles IPX de PF.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Impact de la taille des paquets sur les protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318378"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="5417f-103">Impact de la taille des paquets sur les protocoles</span><span class="sxs-lookup"><span data-stu-id="5417f-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="5417f-104">Les problèmes liés à la taille des paquets multimédias décrits dans la rubrique, [à propos de la taille des paquets multimédias](about-media-packet-size-2.md), affectent différemment les différents \_ protocoles IPX de PF.</span><span class="sxs-lookup"><span data-stu-id="5417f-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="5417f-105">Une stratégie courante pour gérer les différentes contraintes de taille de routeur et de média consiste à utiliser la taille de média complète lorsque le numéro de réseau de la station distante correspond à la station locale, et à revenir à la taille de paquet minimale, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5417f-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="5417f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5417f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5417f-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>\_IPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="5417f-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="5417f-108">Fournit un service de datagrammes ; chaque datagramme doit résider dans la taille de paquet maximale.</span><span class="sxs-lookup"><span data-stu-id="5417f-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="5417f-109">Winsock définit la taille maximale des paquets de datagrammes sur la taille du paquet de média local moins l’en-tête IPX.</span><span class="sxs-lookup"><span data-stu-id="5417f-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="5417f-110">Gardez toutefois à l’esprit que si le paquet est routé, il peut atteindre des restrictions de routeur en cours d’acheminement.</span><span class="sxs-lookup"><span data-stu-id="5417f-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="5417f-111">Assurez-vous que votre application peut revenir à des datagrammes de 546 octets.</span><span class="sxs-lookup"><span data-stu-id="5417f-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="5417f-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="5417f-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="5417f-113">Fournit des services de flux et de paquets séquencés.</span><span class="sxs-lookup"><span data-stu-id="5417f-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="5417f-114">Winsock IPX/SPX permet aux flux de données et aux messages d’être répartis sur plusieurs paquets. par conséquent, la taille des paquets ne limite pas la quantité de données gérées par l' [**envoi**](/windows/desktop/api/Winsock2/nf-winsock2-send) et la [**réception**](/windows/desktop/api/winsock/nf-winsock-recv).</span><span class="sxs-lookup"><span data-stu-id="5417f-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="5417f-115">Toutefois, la taille du média sous-jacent doit être définie correctement ou le premier paquet volumineux sera non remis et la connexion sera réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="5417f-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="5417f-116">Si la station cible se trouve sur le réseau local, Winsock définit sa taille de paquet sur la taille du paquet multimédia.</span><span class="sxs-lookup"><span data-stu-id="5417f-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="5417f-117">Dans le cas contraire, la valeur par défaut est de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="5417f-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="5417f-118">Cette taille peut être modifiée immédiatement après la [**connexion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou l' [**acceptation**](/windows/desktop/api/Winsock2/nf-winsock2-accept) via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="5417f-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="5417f-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII</span><span class="sxs-lookup"><span data-stu-id="5417f-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="5417f-120">SPXII comprend une grande négociation de paquets Internet pour maintenir une taille optimale pour les paquets et ne nécessite pas d’intervention du programmeur.</span><span class="sxs-lookup"><span data-stu-id="5417f-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="5417f-121">Toutefois, si la station à distance ne prend pas en charge SPXII et négocie avec la norme SPX standard, les \_ règles NSPROTO SPX sont activées.</span><span class="sxs-lookup"><span data-stu-id="5417f-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="5417f-122">Protocol</span><span class="sxs-lookup"><span data-stu-id="5417f-122">Protocol</span></span>     | <span data-ttu-id="5417f-123">Multimédia</span><span class="sxs-lookup"><span data-stu-id="5417f-123">Media</span></span>      | <span data-ttu-id="5417f-124">Type</span><span class="sxs-lookup"><span data-stu-id="5417f-124">Type</span></span>        | <span data-ttu-id="5417f-125">Taille des paquets de données</span><span class="sxs-lookup"><span data-stu-id="5417f-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="5417f-126">\_IPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="5417f-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="5417f-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="5417f-127">Ethernet</span></span>   | <span data-ttu-id="5417f-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="5417f-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="5417f-129">802.3</span><span class="sxs-lookup"><span data-stu-id="5417f-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="5417f-130">802.2</span><span class="sxs-lookup"><span data-stu-id="5417f-130">802.2</span></span>       | <span data-ttu-id="5417f-131">1466</span><span class="sxs-lookup"><span data-stu-id="5417f-131">1466</span></span>             |
|              |            | <span data-ttu-id="5417f-132">Snapshots</span><span class="sxs-lookup"><span data-stu-id="5417f-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="5417f-133">Token ring</span><span class="sxs-lookup"><span data-stu-id="5417f-133">Token Ring</span></span> | <span data-ttu-id="5417f-134">4 mégabits</span><span class="sxs-lookup"><span data-stu-id="5417f-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="5417f-135">16 mégabits</span><span class="sxs-lookup"><span data-stu-id="5417f-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="5417f-136">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="5417f-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="5417f-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="5417f-137">Ethernet</span></span>   | <span data-ttu-id="5417f-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="5417f-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="5417f-139">802.3</span><span class="sxs-lookup"><span data-stu-id="5417f-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="5417f-140">802.2</span><span class="sxs-lookup"><span data-stu-id="5417f-140">802.2</span></span>       | <span data-ttu-id="5417f-141">1454</span><span class="sxs-lookup"><span data-stu-id="5417f-141">1454</span></span>             |
|              |            | <span data-ttu-id="5417f-142">Snapshots</span><span class="sxs-lookup"><span data-stu-id="5417f-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="5417f-143">Token ring</span><span class="sxs-lookup"><span data-stu-id="5417f-143">Token Ring</span></span> | <span data-ttu-id="5417f-144">4 mégabits</span><span class="sxs-lookup"><span data-stu-id="5417f-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="5417f-145">16 mégabits</span><span class="sxs-lookup"><span data-stu-id="5417f-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



