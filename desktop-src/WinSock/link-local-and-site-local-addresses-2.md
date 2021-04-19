---
description: Les adresses IPv6 locales et de site local sont appelées adresses étendues.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Adresses IPv6 locales et de site local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515651"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="b0f3f-103">Adresses IPv6 locales et de site local</span><span class="sxs-lookup"><span data-stu-id="b0f3f-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="b0f3f-104">Les adresses IPv6 locales et de site local sont appelées adresses étendues.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="b0f3f-105">L’API Windows Sockets (Winsock) prend en charge le membre d' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) pour une utilisation avec des adresses délimitées.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="b0f3f-106">Pour les adresses IPv6 lien-local (FE80 ::/10 préfixe), le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure **sockaddr \_ in6** est le numéro d’interface.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="b0f3f-107">Pour les adresses locales de site IPv6 (préfixe FEC0 ::/10), le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure **\_ in6 sockaddr** est un identificateur de site.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="b0f3f-108">Voici un exemple d’adresse IPv6 de liaison locale sur \# l’interface 5 :</span><span class="sxs-lookup"><span data-stu-id="b0f3f-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="b0f3f-109">La commande suivante est disponible sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures pour interroger et configurer IPv6 sur un ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="b0f3f-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="b0f3f-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="b0f3f-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="b0f3f-111">Les modifications de configuration effectuées à l’aide des commandes Netsh.exe sont permanentes et ne sont pas perdues lors du redémarrage de l’ordinateur ou du protocole IPv6.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="b0f3f-112">Avant Windows XP avec Service Pack 1 (SP1), la configuration et la gestion IPv6 utilisaient plusieurs anciens outils en ligne de commande (Net.exe, Ipv6.exe et Ipsec6.exe) pour configurer et gérer IPv6.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="b0f3f-113">À l’aide de ces outils plus anciens, les modifications IPv6 ne sont pas permanentes et sont perdues lorsque l’ordinateur ou le protocole IPv6 a été redémarré.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="b0f3f-114">Ces anciens outils en ligne de commande sont uniquement pris en charge sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="b0f3f-115">Sur Windows XP avec SP1, la commande suivante affiche la liste des interfaces IPv6 sur un ordinateur local, y compris l’index d’interface, le nom de l’interface et diverses autres propriétés de l’interface.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="b0f3f-116">**netsh interface ipv6 show interface**</span><span class="sxs-lookup"><span data-stu-id="b0f3f-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="b0f3f-117">Sur Windows XP avec SP1, la commande suivante permet de modifier l’identificateur de site associé à un index d’interface.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="b0f3f-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid = valeur**</span><span class="sxs-lookup"><span data-stu-id="b0f3f-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="b0f3f-119">Sur Windows XP, la commande antérieure suivante remplacera également l’identificateur de site associé à une adresse de site local par 3.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="b0f3f-120">**FEC0 RTU IPv6 ::/10 3**</span><span class="sxs-lookup"><span data-stu-id="b0f3f-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="b0f3f-121">Si vous envoyez ou vous vous connectez à une adresse délimitée, le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) peut être laissé non spécifié (zéro), ce qui représente une adresse étendue ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="b0f3f-122">Par exemple, l’adresse lien-local suivante est ambiguë :</span><span class="sxs-lookup"><span data-stu-id="b0f3f-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="b0f3f-123">Si vous effectuez une liaison à une adresse délimitée, le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**\_ in6 sockaddr**](sockaddr-2.md) doit contenir une valeur différente de zéro qui spécifie un numéro d’interface valide pour une adresse lien-local ou un identificateur de site pour une adresse de site local.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="b0f3f-124">Adresses étendues ambiguës</span><span class="sxs-lookup"><span data-stu-id="b0f3f-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="b0f3f-125">Si vous envoyez ou vous vous connectez à une adresse délimitée et que vous n’avez pas spécifié le membre de l' **\_ \_ ID d’étendue Sin6** dans la structure [**sockaddr \_ in6**](sockaddr-2.md) , l’adresse étendue est ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="b0f3f-126">Pour résoudre ce comportement, le protocole IPv6 détermine d’abord si vous avez lié le socket à une adresse source.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="b0f3f-127">Si c’est le cas, l’adresse source liée résout l’ambiguïté en fournissant un numéro d’interface ou un identificateur de site.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="b0f3f-128">Si vous envoyez ou vous vous connectez à une adresse délimitée et que vous n’avez pas spécifié le membre de l' **\_ \_ ID d’étendue Sin6** ou lié une adresse source, le protocole IPv6 vérifie la table de routage.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="b0f3f-129">Par exemple, la commande suivante affiche la table de routage IPv6 sur un ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="b0f3f-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="b0f3f-130">**netsh interface ipv6 show route**</span><span class="sxs-lookup"><span data-stu-id="b0f3f-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="b0f3f-131">Cela indique que les adresses lien-local sont traitées par défaut en tant que liens sur les interfaces \# 13 et \# 14.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="b0f3f-132">Une ambiguïté se produit lorsqu’un ordinateur local possède plusieurs cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="b0f3f-133">Par exemple, la commande **netsh** ci-dessus indique qu’il existe deux interfaces réseau (connexion au réseau local et connexion réseau sans fil).</span><span class="sxs-lookup"><span data-stu-id="b0f3f-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="b0f3f-134">Lorsqu’une application spécifie une adresse lien-local de destination (FE80 :: 10, par exemple) sans ID d’étendue, il n’est pas évident de savoir quel adaptateur utiliser pour envoyer le paquet.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="b0f3f-135">Seule une monodiffusion de liaison locale de liaison (FE80 ::/64) ou une adresse de destination IPv6 de multidiffusion d’étendue de liaison (FF00 ::/8) peut être affectée de l’absence d’un ID d’étendue lors de l’envoi d’un paquet.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="b0f3f-136">Découverte de voisin</span><span class="sxs-lookup"><span data-stu-id="b0f3f-136">Neighbor Discovery</span></span>

<span data-ttu-id="b0f3f-137">Si vous n’avez pas spécifié le membre de l' **\_ \_ ID de l’étendue Sin6** dans la structure [**\_ in6 sockaddr**](sockaddr-2.md) , que vous n’avez pas lié une adresse source et que vous n’avez pas spécifié d’itinéraire pour les adresses lien-local, le protocole IPv6 essaiera la découverte du voisin pour résoudre l’adresse lien-local de destination.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="b0f3f-138">Pour un paquet donné en cours d’envoi, une interface est tentée.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="b0f3f-139">Cette première interface qui est tentée est considérée comme l’interface la plus préférée.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="b0f3f-140">Si la découverte de voisins ne parvient pas à résoudre l’adresse lien-local sur une interface, le paquet à envoyer est supprimé et le système se souvient que l’adresse lien-local de destination n’est pas accessible sur cette interface.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="b0f3f-141">Sur le paquet suivant à envoyer dans les mêmes conditions, une interface différente est tentée pour la découverte de voisins.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="b0f3f-142">Ce processus continue à traverser chacune des interfaces sur un ordinateur local pour chaque nouveau paquet jusqu’à ce que la découverte du voisin réponde pour l’adresse lien-local de destination ou que toutes les interfaces possibles aient été essayées et échouées.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="b0f3f-143">Chaque fois qu’une tentative de résolution du voisin échoue, une interface est supprimée pour ce voisin.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="b0f3f-144">Si l’adresse lien-local de destination est résolue, cette interface est utilisée pour envoyer le paquet actuel.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="b0f3f-145">Cette interface est également utilisée pour tous les paquets de portée ambiguë suivants qui sont envoyés à la même adresse de destination lien-local.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="b0f3f-146">Si la découverte de voisins ne parvient pas à résoudre l’adresse lien-local de destination sur toutes les interfaces, le système tente alors d’envoyer le paquet sur l’interface la plus préférée (la première interface essayée).</span><span class="sxs-lookup"><span data-stu-id="b0f3f-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="b0f3f-147">La pile réseau continue de tenter de résoudre l’adresse lien-local de destination sur l’interface la plus préférée.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="b0f3f-148">Après un certain laps de temps après l’échec de la découverte de voisins sur toutes les interfaces, la pile réseau redémarre le processus et tente de résoudre l’adresse lien-local de destination sur toutes les interfaces.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="b0f3f-149">Actuellement, cet intervalle de temps pendant lequel la découverte du voisin est de nouveau effectuée sur toutes les interfaces est de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="b0f3f-150">Toutefois, cet intervalle de temps peut changer sur les versions de Windows et ne doit pas être utilisé par une application.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="b0f3f-151">Si une application lie la même adresse lien-local à une autre interface après que la découverte du voisin a résolu l’adresse lien-local, cela ne remplace pas l’interface par l’adresse de destination lien-local renvoyée par la découverte de voisins.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="b0f3f-152">Pour plus d’informations sur la découverte de voisins pour IP version 6, consultez [RFC4861](https://tools.ietf.org/html/rfc4861) publié par l’IETF.</span><span class="sxs-lookup"><span data-stu-id="b0f3f-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0f3f-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0f3f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f3f-154">Préfixes de site IPv6</span><span class="sxs-lookup"><span data-stu-id="b0f3f-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="b0f3f-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="b0f3f-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="b0f3f-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="b0f3f-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="b0f3f-157">Utilisation d'une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="b0f3f-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



