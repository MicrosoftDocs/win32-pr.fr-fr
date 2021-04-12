---
title: Application de la couche application (ALE)
description: ALE est un ensemble de couches en mode noyau de plateforme de filtrage Windows (WFP) qui sont utilisées pour le filtrage avec état.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381908"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="27f60-103">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="27f60-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="27f60-104">ALE est un ensemble de couches en mode noyau de plateforme de filtrage Windows (WFP) qui sont utilisées pour le filtrage avec état.</span><span class="sxs-lookup"><span data-stu-id="27f60-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="27f60-105">Le filtrage avec État assure le suivi de l’état des connexions réseau et autorise uniquement les paquets qui correspondent à un état de connexion connu.</span><span class="sxs-lookup"><span data-stu-id="27f60-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="27f60-106">Par exemple, le filtrage avec état d’une connexion TCP lancée à partir d’un pare-feu peut autoriser uniquement les paquets entrants qui correspondent aux paquets sortants précédents envoyés par le tiers protégé.</span><span class="sxs-lookup"><span data-stu-id="27f60-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="27f60-107">Les filtres dans les couches ALE autorisent la création de connexions entrantes et sortantes, les affectations de port, les opérations de socket telles que [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la création de sockets bruts et le mode de proximité.</span><span class="sxs-lookup"><span data-stu-id="27f60-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="27f60-108">Le trafic au niveau des couches ALE est classé par opération par connexion ou par socket.</span><span class="sxs-lookup"><span data-stu-id="27f60-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="27f60-109">Sur les couches non ALE, les filtres peuvent uniquement classer le trafic par paquet.</span><span class="sxs-lookup"><span data-stu-id="27f60-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="27f60-110">Les couches ALE sont les seules couches WFP où le trafic réseau peut être filtré en fonction de l’identité de l’application (à l’aide d’un nom de fichier normalisé) et en fonction de l’identité de l’utilisateur, à l’aide d’un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="27f60-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="27f60-111">(Voir FLT \_ \_ \_ Informations sur le nom de fichier dans la documentation du kit de pilotes Windows (WDK), pour plus d’informations sur les noms de fichiers normalisés.)</span><span class="sxs-lookup"><span data-stu-id="27f60-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="27f60-112">En outre, quand IPsec est utilisé pour sécuriser la connexion, le filtrage au niveau des couches ALE peut également être effectué sur l’identité de l’ordinateur distant et sur l’identité de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="27f60-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="27f60-113">Les identités de l’ordinateur distant et de l’utilisateur sont obtenues à partir des informations d’identification utilisées lors de la création d’une session IPsec.</span><span class="sxs-lookup"><span data-stu-id="27f60-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="27f60-114">Pour cette raison, les stratégies qui appliquent (par exemple, « administrateur ») et/ou l’application (par exemple, « Internet Explorer ») sont autorisées à effectuer les opérations de réseau mentionnées ci-dessus sont créées au niveau des couches ALE.</span><span class="sxs-lookup"><span data-stu-id="27f60-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="27f60-115">ALE fournit la mise en application pour les stratégies telles que « autoriser tout accès à Windows Messenger sur le réseau tout en bloquant toutes les autres applications ».</span><span class="sxs-lookup"><span data-stu-id="27f60-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="27f60-116">Dans un tel exemple, lorsque l’application « Messenger » se connecte sur le réseau, ALE interrompt l’événement, détermine qu’elle a été lancée par Messenger et interroge le moteur de filtre WFP pour déterminer si le socket doit être autorisé à continuer.</span><span class="sxs-lookup"><span data-stu-id="27f60-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="27f60-117">En raison de la nature des véritables sockets à deux adresses IP, les classifications au niveau de la couche ALE d’IPv4 peuvent ne pas se produire.</span><span class="sxs-lookup"><span data-stu-id="27f60-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="27f60-118">Cela est dû à la conception, car pour toutes les intentions et les objectifs, le socket est un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="27f60-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="27f60-119">Pour voir le trafic v4 pour un tel Socket, créez des filtres au niveau de la couche V6 à l’aide de l’adresse mappée IPv6.</span><span class="sxs-lookup"><span data-stu-id="27f60-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="27f60-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27f60-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f60-121">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="27f60-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="27f60-122">Filtrage avec état ALE</span><span class="sxs-lookup"><span data-stu-id="27f60-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="27f60-123">Trafic de diffusion/multidiffusion ALE</span><span class="sxs-lookup"><span data-stu-id="27f60-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="27f60-124">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="27f60-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="27f60-125">Personnalisation du fluide ALE</span><span class="sxs-lookup"><span data-stu-id="27f60-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 