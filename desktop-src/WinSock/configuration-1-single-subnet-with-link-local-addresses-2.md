---
description: La première configuration ne nécessite pas de configuration supplémentaire au-delà de l’installation du protocole Microsoft IPv6 Technology Preview.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Configuration 1 : sous-réseau unique avec adresses lien-local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033986"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="bb442-103">Configuration 1 : sous-réseau unique avec adresses lien-local</span><span class="sxs-lookup"><span data-stu-id="bb442-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="bb442-104">La première configuration ne nécessite pas de configuration supplémentaire au-delà de l’installation du protocole Microsoft IPv6 Technology Preview.</span><span class="sxs-lookup"><span data-stu-id="bb442-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="bb442-105">Cette configuration se compose d’au moins deux nœuds sur le même sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="bb442-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="bb442-106">Dans la terminologie IPv6, les deux nœuds se trouvent sur le même lien sans routeurs intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="bb442-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="bb442-107">L’illustration suivante montre la configuration de deux nœuds sur un sous-réseau unique à l’aide d’adresses lien-local.</span><span class="sxs-lookup"><span data-stu-id="bb442-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![deux nœuds utilisant des adresses lien-local.](images/v6mig-1.png)

<span data-ttu-id="bb442-109">Par défaut, IPv6 configure les adresses IP de lien local pour chaque interface correspondant aux cartes réseau Ethernet installées.</span><span class="sxs-lookup"><span data-stu-id="bb442-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="bb442-110">Les adresses lien-local ont le préfixe FE80 ::/64.</span><span class="sxs-lookup"><span data-stu-id="bb442-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="bb442-111">Les 64 derniers bits de l’adresse IPv6 sont appelés identificateurs d’interface et sont dérivés de l’adresse MAC 48 bits de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="bb442-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="bb442-112">Pour créer l’identificateur d’interface IPv6 à partir de l’adresse MAC Ethernet 48 bits (6 octets) :</span><span class="sxs-lookup"><span data-stu-id="bb442-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="bb442-113">Les chiffres hexadécimaux 0xFF-Fe sont insérés entre le troisième et le quatrième octet de l’adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="bb442-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="bb442-114">Le bit universel/local, le deuxième bit de poids faible du premier octet de l’adresse MAC, est complété.</span><span class="sxs-lookup"><span data-stu-id="bb442-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="bb442-115">S’il s’agit d’un 1, il prend la valeur 0 et, s’il s’agit d’un 0, il est converti en 1.</span><span class="sxs-lookup"><span data-stu-id="bb442-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="bb442-116">Par exemple, pour l’adresse MAC 00-60-08-52-F9-D8 :</span><span class="sxs-lookup"><span data-stu-id="bb442-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="bb442-117">Les chiffres hexadécimaux 0xFF-Fe sont insérés entre 0x08 (le troisième octet) et 0x52 (quatrième octet) de l’adresse MAC, formant l’adresse 64 bits 00-60-08-FF-Fe-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="bb442-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="bb442-118">Le bit universel/local, le deuxième bit de poids faible de 0x00 (le premier octet) de l’adresse MAC est complété.</span><span class="sxs-lookup"><span data-stu-id="bb442-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="bb442-119">Le deuxième bit de poids faible de 0x00 est 0, qui, lorsqu’il est complété, devient 1.</span><span class="sxs-lookup"><span data-stu-id="bb442-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="bb442-120">Le résultat est que, pour le premier octet, 0x00 devient 0x02.</span><span class="sxs-lookup"><span data-stu-id="bb442-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="bb442-121">Par conséquent, l’identificateur d’interface IPv6 correspondant à l’adresse MAC Ethernet 00-60-08-52-F9-D8 est 02-60-08-FF-Fe-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="bb442-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="bb442-122">L’adresse lien-local d’un nœud est la combinaison du préfixe FE80 ::/64 et de l’identificateur d’interface 64 bits, exprimée en notation hexadécimale à deux-points IPv6.</span><span class="sxs-lookup"><span data-stu-id="bb442-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="bb442-123">Par conséquent, l’adresse lien-local de cet exemple de nœud avec le préfixe FE80 ::/64 et l’identificateur d’interface 02-60-08-FF-Fe-52-F9-D8 est FE80 :: 260:8FF : FE52 : F9D8.</span><span class="sxs-lookup"><span data-stu-id="bb442-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="bb442-124">Vous pouvez afficher votre adresse de lien local à l’aide de IPv6 si, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="bb442-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="bb442-125">**IPv6 si**</span><span class="sxs-lookup"><span data-stu-id="bb442-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="bb442-126">L’interface 4 est une interface qui correspond à une carte Ethernet installée avec l’adresse lien-local FE80 :: 210:5aff : FEAA : 20a2.</span><span class="sxs-lookup"><span data-stu-id="bb442-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="bb442-127">Pour plus d’informations sur l’adressage IPv6 et une vue d’ensemble des concepts IPv6, consultez le livre blanc Introduction à IPv6.</span><span class="sxs-lookup"><span data-stu-id="bb442-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="bb442-128">Test de la connectivité entre deux hôtes lien-local</span><span class="sxs-lookup"><span data-stu-id="bb442-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="bb442-129">Vous pouvez effectuer une requête ping simple (échange de messages ICMPv6 de demande d’écho et de réponse à écho) à l’aide de IPv6 entre deux hôtes lien-local.</span><span class="sxs-lookup"><span data-stu-id="bb442-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="bb442-130">**Pour exécuter une commande ping à l’aide d’IPv6 entre deux hôtes lien-local**</span><span class="sxs-lookup"><span data-stu-id="bb442-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="bb442-131">Installez la version préliminaire de la technologie Microsoft IPv6 pour Windows sur deux hôtes Windows (hôte A et hôte B) qui se trouvent sur le même lien (sous-réseau).</span><span class="sxs-lookup"><span data-stu-id="bb442-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="bb442-132">Utilisez IPv6 si sur l’hôte A pour obtenir l’adresse lien-local de l’interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="bb442-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="bb442-133">Exemple : l’adresse lien-local de l’hôte A est FE80 :: 210:5aff : FEAA : 20a2.</span><span class="sxs-lookup"><span data-stu-id="bb442-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="bb442-134">Utilisez IPv6 si sur l’hôte B pour obtenir l’adresse lien-local de l’interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="bb442-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="bb442-135">Exemple : l’adresse lien-local de l’hôte B est FE80 :: 260:97FF : FE02:6EA5.</span><span class="sxs-lookup"><span data-stu-id="bb442-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="bb442-136">À partir de l’hôte A, exécutez une commande ping sur l’hôte B avec Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="bb442-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="bb442-137">Exemple : ping6 FE80 :: 260:97FF : FE02:6EA5</span><span class="sxs-lookup"><span data-stu-id="bb442-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="bb442-138">Pour spécifier l’adresse source à partir de laquelle les messages de demande d’écho sont envoyés, vous pouvez également utiliser l’option Ping6.exe-s.</span><span class="sxs-lookup"><span data-stu-id="bb442-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="bb442-139">Par exemple, pour envoyer des demandes d’écho à l’hôte B à partir de l’adresse IPv6 FE80 :: 210:5aff : FEAA : 20a2, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bb442-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="bb442-140">**ping6-s FE80 :: 210:5aff : FEAA : 20a2% 4 FE80 :: 260:97FF : FE02:6EA5**</span><span class="sxs-lookup"><span data-stu-id="bb442-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="bb442-141">Lors du test ping d’une adresse de lien local ou de site local, il est recommandé de spécifier l’ID d’étendue pour rendre l’adresse de destination non ambiguë.</span><span class="sxs-lookup"><span data-stu-id="bb442-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="bb442-142">La notation permettant de spécifier l’ID de portée est adresse% Scope-ID.</span><span class="sxs-lookup"><span data-stu-id="bb442-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="bb442-143">Pour les adresses lien-local, l’ID d’étendue est égal au numéro d’interface tel qu’il est affiché dans la commande IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="bb442-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="bb442-144">Pour les adresses locales de site, l’ID d’étendue est égal au numéro de site tel qu’il est affiché dans la commande IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="bb442-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="bb442-145">Par exemple, pour envoyer des messages de demande d’écho à l’hôte B à l’aide de l’ID de portée 4, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bb442-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="bb442-146">**ping6 FE80 :: 260:97FF : FE02:6EA5% 4**</span><span class="sxs-lookup"><span data-stu-id="bb442-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb442-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bb442-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb442-148">Configurations recommandées pour IPv6</span><span class="sxs-lookup"><span data-stu-id="bb442-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



