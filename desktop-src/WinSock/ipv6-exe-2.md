---
description: Toutes les configurations IPv6 sont effectuées à l’aide de l’outil Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201428"
---
# <a name="ipv6exe"></a><span data-ttu-id="9b36f-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="9b36f-103">Ipv6.exe</span></span>

<span data-ttu-id="9b36f-104">Toutes les configurations IPv6 sont effectuées à l’aide de l’outil Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="9b36f-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="9b36f-105">Cet outil est principalement utilisé pour l’interrogation et la configuration des interfaces, des adresses, des caches et des itinéraires IPv6.</span><span class="sxs-lookup"><span data-stu-id="9b36f-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="9b36f-106">Les sous-commandes IPv6 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9b36f-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="9b36f-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 si** \[ que\#\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-108">Affiche des informations sur les interfaces.</span><span class="sxs-lookup"><span data-stu-id="9b36f-108">Displays information about interfaces.</span></span> <span data-ttu-id="9b36f-109">Si un numéro d’interface est spécifié, seules les informations relatives à cette interface sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="9b36f-110">Dans le cas contraire, des informations sur toutes les interfaces sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="9b36f-111">La sortie inclut l’adresse de la couche de liaison de l’interface et la liste des adresses IPv6 affectées à l’interface, y compris l’unité de transmission maximale actuelle de l’interface et la MTU maximale (true) que l’interface peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="9b36f-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="9b36f-112">L’interface \# 1 est une pseudo-interface utilisée pour le bouclage.</span><span class="sxs-lookup"><span data-stu-id="9b36f-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="9b36f-113">L’interface \# 2 est une pseudo-interface utilisée pour le tunneling configuré, le tunneling automatique et le tunneling 6to4.</span><span class="sxs-lookup"><span data-stu-id="9b36f-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="9b36f-114">Les autres interfaces sont numérotées de façon séquentielle dans l’ordre dans lequel elles sont créées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="9b36f-115">Cet ordre varie d’un ordinateur à un autre.</span><span class="sxs-lookup"><span data-stu-id="9b36f-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="9b36f-116">Les adresses de couche de liaison au format *AA* - *BB* - *CC* - *JJ* - *EE* - *FF* sont des adresses Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9b36f-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="9b36f-117">Adresse de couche de liaison dans *un*. *b*. *c*. la forme *d* sont des interfaces 6-sur-4.</span><span class="sxs-lookup"><span data-stu-id="9b36f-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="9b36f-118">Pour plus d’informations sur 6-sur-4, consultez la RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="9b36f-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="9b36f-119">Les deux pseudo-interfaces n’utilisent pas la découverte du voisin IPv6.</span><span class="sxs-lookup"><span data-stu-id="9b36f-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IFC IPv6** si \# \[ transfère \] \[ \] \[ des publications-transfère \] \[ -publie les \] \[ octets MTU site \# site \] \[ -identifier\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-121">Contrôle les attributs d’interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-121">Controls interface attributes.</span></span> <span data-ttu-id="9b36f-122">Les interfaces peuvent être transférées, auquel cas elles transfèrent les paquets avec des adresses de destination non attribuées à l’interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="9b36f-123">Les interfaces peuvent être publicitaires, auquel cas elles envoient des publications de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="9b36f-124">Ces attributs peuvent être contrôlés indépendamment.</span><span class="sxs-lookup"><span data-stu-id="9b36f-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="9b36f-125">Une interface envoie les sollicitations de routeur et reçoit les annonces de routeur, ou reçoit les sollicitations de routeur et envoie les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="9b36f-126">Étant donné que les deux pseudo-interfaces n’utilisent pas la découverte de voisins, elles ne peuvent pas être configurées pour envoyer des annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="9b36f-127">Les transferts peuvent être abrégés en FORW et publiés comme adv.</span><span class="sxs-lookup"><span data-stu-id="9b36f-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="9b36f-128">L’unité MTU de l’interface peut également être définie.</span><span class="sxs-lookup"><span data-stu-id="9b36f-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="9b36f-129">La nouvelle unité de transmission maximale (MTU) doit être inférieure ou égale à l’unité de transmission maximale (true) du lien (comme indiqué par IPv6 si) et supérieure ou égale à l’unité MTU IPv6 minimale (1280 octets).</span><span class="sxs-lookup"><span data-stu-id="9b36f-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="9b36f-130">L’identificateur de site d’une interface peut également être modifié.</span><span class="sxs-lookup"><span data-stu-id="9b36f-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="9b36f-131">Les identificateurs de site sont utilisés dans \_ le \_ champ ID d’étendue Sin6 avec des adresses de site local.</span><span class="sxs-lookup"><span data-stu-id="9b36f-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** si\#</span><span class="sxs-lookup"><span data-stu-id="9b36f-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-133">Supprime une interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-133">Deletes an interface.</span></span> <span data-ttu-id="9b36f-134">Les pseudo-interfaces de bouclage et de tunnel ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**contexte de nommage IPv6** \[ \# \[ adresse if\]\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-136">Affiche le contenu du cache du voisin.</span><span class="sxs-lookup"><span data-stu-id="9b36f-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="9b36f-137">Si un numéro d’interface est spécifié, seul le contenu du cache du voisin de cette interface est affiché.</span><span class="sxs-lookup"><span data-stu-id="9b36f-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="9b36f-138">Sinon, le contenu de tous les caches voisins de l’interface est affiché.</span><span class="sxs-lookup"><span data-stu-id="9b36f-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="9b36f-139">Si une interface est spécifiée, une adresse IPv6 peut être spécifiée pour afficher uniquement cette entrée de cache du voisin.</span><span class="sxs-lookup"><span data-stu-id="9b36f-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="9b36f-140">Pour chaque entrée de cache du voisin, l’interface, l’adresse IPv6, l’adresse de couche de liaison et l’état d’atteinte sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**IPv6 NCF** \[ \# \[ adresse if\]\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-142">Vide les entrées de cache du voisin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="9b36f-143">Seules les entrées de cache du voisin sans références sont purgées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="9b36f-144">Étant donné que les entrées du cache d’itinéraire contiennent des références aux entrées de cache du voisin, le cache d’itinéraire doit d’abord être vidé.</span><span class="sxs-lookup"><span data-stu-id="9b36f-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="9b36f-145">Les entrées de la table de routage peuvent également contenir des références aux entrées du cache du voisin.</span><span class="sxs-lookup"><span data-stu-id="9b36f-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**RC IPv6** \[ \# adresse if\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-147">Affiche le contenu du cache d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="9b36f-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="9b36f-148">Le cache d’itinéraire est le nom de l’implémentation Microsoft IPv6 pour le cache de destination.</span><span class="sxs-lookup"><span data-stu-id="9b36f-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="9b36f-149">Si une interface et une adresse sont spécifiées, l’entrée du cache d’itinéraire pour atteindre l’adresse par le biais de l’interface s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9b36f-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="9b36f-150">Dans le cas contraire, toutes les entrées du cache d’itinéraire sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="9b36f-151">Pour chaque entrée du cache d’itinéraire, l’adresse IPv6 et l’interface du saut suivant et l’adresse voisin sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="9b36f-152">L’adresse source par défaut à utiliser avec cette destination, la MTU de chemin actuelle pour atteindre cette destination via l’interface et la détermination de l’existence d’une entrée spécifique à l’interface-cache de routage sont également affichées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="9b36f-153">Toute adresse de précaution (pour la mobilité) pour l’adresse de destination s’affiche également.</span><span class="sxs-lookup"><span data-stu-id="9b36f-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="9b36f-154">Une adresse de destination peut avoir plusieurs entrées de cache d’itinéraires (autant qu’une adresse pour chaque interface sortante).</span><span class="sxs-lookup"><span data-stu-id="9b36f-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="9b36f-155">Toutefois, une adresse de destination peut avoir au maximum une entrée du cache d’itinéraire qui n’est pas spécifique à l’interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="9b36f-156">Une entrée spécifique à l’interface du cache d’itinéraire est utilisée uniquement si l’application spécifie explicitement cette interface sortante.</span><span class="sxs-lookup"><span data-stu-id="9b36f-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ \# \[ adresse if\]\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-158">Vide les entrées du cache d’itinéraire spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC IPv6**</span><span class="sxs-lookup"><span data-stu-id="9b36f-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-160">Affiche le contenu du cache de liaison, qui contient les liaisons entre les adresses d’hébergement et les adresses d’hébergement pour Mobile IPv6.</span><span class="sxs-lookup"><span data-stu-id="9b36f-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="9b36f-161">Pour chaque liaison, l’adresse d’hébergement, l’adresse d’hébergement, le numéro de séquence de liaison et la durée de vie sont affichés.</span><span class="sxs-lookup"><span data-stu-id="9b36f-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 Adu** si \# /address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[ monodiffusion\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-163">Ajoute ou supprime une attribution d’adresse monodiffusion ou anycast sur une interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="9b36f-164">L’adresse de monodiffusion est traitée si anycast n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b36f-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="9b36f-165">La durée de vie est infinie si elle n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b36f-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="9b36f-166">Si seule une durée de vie valide est spécifiée, la durée de vie préférée est égale à la durée de vie valide.</span><span class="sxs-lookup"><span data-stu-id="9b36f-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="9b36f-167">Une durée de vie infinie peut être spécifiée, ou une valeur finie en secondes.</span><span class="sxs-lookup"><span data-stu-id="9b36f-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="9b36f-168">La durée de vie préférée doit être inférieure ou égale à la durée de vie valide.</span><span class="sxs-lookup"><span data-stu-id="9b36f-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="9b36f-169">La spécification d’une durée de vie de zéro entraîne la suppression de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="9b36f-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="9b36f-170">Vous pouvez abréger la durée de vie en tant que vie.</span><span class="sxs-lookup"><span data-stu-id="9b36f-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="9b36f-171">Pour les adresses anycast, les seules valeurs de durée de vie valides sont zéro et Infinite.</span><span class="sxs-lookup"><span data-stu-id="9b36f-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**SPT IPv6**</span><span class="sxs-lookup"><span data-stu-id="9b36f-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-173">Affiche le contenu actuel de la table de préfixe de site.</span><span class="sxs-lookup"><span data-stu-id="9b36f-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="9b36f-174">Pour chaque préfixe de site, la commande affiche le préfixe, l’interface à laquelle le préfixe de site s’applique et la durée de vie du préfixe, en secondes.</span><span class="sxs-lookup"><span data-stu-id="9b36f-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="9b36f-175">Les préfixes de site sont normalement configurés automatiquement à partir des annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="9b36f-176">Ils sont utilisés dans la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) pour filtrer les adresses locales de site inappropriées.</span><span class="sxs-lookup"><span data-stu-id="9b36f-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>préfixe **SPU IPv6** si \# \[ durée de vie L\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-178">Ajoute, supprime ou met à jour un préfixe dans la table de préfixe de site.</span><span class="sxs-lookup"><span data-stu-id="9b36f-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="9b36f-179">Le préfixe et le numéro d’interface sont requis.</span><span class="sxs-lookup"><span data-stu-id="9b36f-179">The prefix and interface number are required.</span></span> <span data-ttu-id="9b36f-180">La durée de vie du préfixe de site, spécifiée en secondes, est définie par défaut sur Infinite s’il n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b36f-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="9b36f-181">Si vous spécifiez une durée de vie de zéro, le préfixe de site est supprimé.</span><span class="sxs-lookup"><span data-stu-id="9b36f-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="9b36f-182">Cette commande n’est pas nécessaire pour la configuration normale des ordinateurs hôtes ou routeurs.</span><span class="sxs-lookup"><span data-stu-id="9b36f-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**RT IPv6**</span><span class="sxs-lookup"><span data-stu-id="9b36f-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-184">Affiche le contenu actuel de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="9b36f-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="9b36f-185">Pour chaque entrée de table de routage, la commande affiche le préfixe d’itinéraire, une interface on-Link ou un voisin de saut suivant sur une interface, une valeur de préférence (plus petite est préférable) et une durée de vie en secondes.</span><span class="sxs-lookup"><span data-stu-id="9b36f-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="9b36f-186">Les entrées de la table de routage peuvent également avoir des attributs **Publish** et **Aging** .</span><span class="sxs-lookup"><span data-stu-id="9b36f-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="9b36f-187">Par défaut, ils vieillissent (la durée de vie est inférieure à la constante restante) et ne sont pas publiés (ils ne sont pas utilisés dans la construction des publications de routeur).</span><span class="sxs-lookup"><span data-stu-id="9b36f-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="9b36f-188">Sur les ordinateurs hôtes, les entrées de la table de routage sont normalement configurées automatiquement à partir des annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="9b36f-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>préfixe **RTU IPv6** si \# \[ /nexthop \] \[ durée de vie \] \[ de la préférence P \] \[ publication \] \[ âge du \] \[ site-préfixe-longueur\]</span><span class="sxs-lookup"><span data-stu-id="9b36f-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="9b36f-190">Ajoute ou supprime un itinéraire dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="9b36f-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="9b36f-191">Le préfixe d’itinéraire est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b36f-191">The route prefix is required.</span></span> <span data-ttu-id="9b36f-192">Le préfixe peut être défini sur un lien vers une interface spécifiée, ou un tronçon suivant, spécifié avec une adresse voisine sur une interface.</span><span class="sxs-lookup"><span data-stu-id="9b36f-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="9b36f-193">L’itinéraire peut avoir une durée de vie en secondes, avec la valeur par défaut infinie et une préférence, avec la valeur par défaut zéro ou la plus préférée.</span><span class="sxs-lookup"><span data-stu-id="9b36f-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="9b36f-194">Si vous spécifiez une durée de vie de zéro, l’itinéraire est supprimé.</span><span class="sxs-lookup"><span data-stu-id="9b36f-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="9b36f-195">Si la route est spécifiée en tant que publication, indiquant qu’elle sera utilisée dans la construction des publications de routeur, elle n’a pas d’ancienneté.</span><span class="sxs-lookup"><span data-stu-id="9b36f-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="9b36f-196">La durée de vie de l’itinéraire n’est pas comptabilisée et est par conséquent infinie, mais la valeur est utilisée dans les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="9b36f-197">Si vous le souhaitez, un itinéraire peut être spécifié comme un itinéraire publié qui vieillit également.</span><span class="sxs-lookup"><span data-stu-id="9b36f-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="9b36f-198">Par défaut, un itinéraire non publié passe toujours à l’âge.</span><span class="sxs-lookup"><span data-stu-id="9b36f-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="9b36f-199">La sous-option SPL facultative peut être utilisée pour spécifier une longueur de préfixe de site associée à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="9b36f-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="9b36f-200">La longueur de préfixe de site est utilisée uniquement lors de l’envoi d’annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="9b36f-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="9b36f-201">La durée de vie peut être abrégée en vie, préférence en tant que préférences et publier en tant que pub.</span><span class="sxs-lookup"><span data-stu-id="9b36f-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



