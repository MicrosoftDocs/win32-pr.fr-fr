---
description: 6to4 est une méthode permettant de connecter des hôtes ou des sites IPv6 sur l’infrastructure Internet IPv4 existante.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuration 2 : trafic IPv6 entre les nœuds de différents sous-réseaux d’un interréseau IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484952"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="45b36-103">Configuration 2 : trafic IPv6 entre les nœuds de différents sous-réseaux d’un interréseau IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="45b36-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="45b36-104">6to4 est une méthode permettant de connecter des hôtes ou des sites IPv6 sur l’infrastructure Internet IPv4 existante.</span><span class="sxs-lookup"><span data-stu-id="45b36-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="45b36-105">Elle utilise un préfixe d’adresse unique pour fournir aux sites IPv6 isolés leur propre espace d’adressage IPv6.</span><span class="sxs-lookup"><span data-stu-id="45b36-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="45b36-106">6to4 est semblable à un « Pseudo-ISP » fournissant une connectivité IPv6.</span><span class="sxs-lookup"><span data-stu-id="45b36-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="45b36-107">Vous pouvez utiliser 6to4 pour communiquer directement avec d’autres sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="45b36-108">6to4 ne requiert pas l’utilisation de routeurs IPv6 et son trafic IPv6 est encapsulé avec un en-tête IPv4.</span><span class="sxs-lookup"><span data-stu-id="45b36-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="45b36-109">L’illustration suivante montre la configuration de deux nœuds sur des sous-réseaux distincts à l’aide de 6to4 pour communiquer sur un routeur IPv4.</span><span class="sxs-lookup"><span data-stu-id="45b36-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![les nœuds qui utilisent 6to4 pour communiquer sur un routeur IPv4.](images/v6mig-2.png)

<span data-ttu-id="45b36-111">La principale exigence d’utiliser 6to4 est une adresse IPv4 globalement routable pour votre site.</span><span class="sxs-lookup"><span data-stu-id="45b36-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="45b36-112">Supposons que votre site se compose d’un ensemble d’ordinateurs IPv6 que vous gérez (certains exécutant le protocole Microsoft IPv6 et d’autres implémentations IPv6).</span><span class="sxs-lookup"><span data-stu-id="45b36-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="45b36-113">Supposons également que tous les ordinateurs IPv6 sont connectés directement via Ethernet ou 6-sur-4.</span><span class="sxs-lookup"><span data-stu-id="45b36-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="45b36-114">L’adresse IPv4 globalement routable doit être affectée à l’un de vos ordinateurs exécutant le protocole Microsoft IPv6.</span><span class="sxs-lookup"><span data-stu-id="45b36-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="45b36-115">Cet ordinateur sera votre passerelle 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="45b36-116">Si vous disposez d’une adresse IPv4 qui fait partie de l’espace d’adressage privé (10.0.0.0/8, 172.16.0.0/12 ou 192.168.0.0/16) ou de l’espace d’adressage APIPA (Automatic Private IP Addressing) de 169.254.0.0/16 utilisé par Windows 2000, elle n’est pas globalement routable.</span><span class="sxs-lookup"><span data-stu-id="45b36-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="45b36-117">Dans le cas contraire, il s’agit probablement d’une adresse IP publique qui est globalement routable.</span><span class="sxs-lookup"><span data-stu-id="45b36-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="45b36-118">Pour plus d’informations sur la prise en charge de 6to4, consultez la rubrique [débogage de la configuration 6to4](#debugging-6to4-configuration) dans ce document.</span><span class="sxs-lookup"><span data-stu-id="45b36-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="45b36-119">Outil 6to4cfg.exe</span><span class="sxs-lookup"><span data-stu-id="45b36-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="45b36-120">L’outil 6to4cfg.exe automatise la configuration 6to4, découvre automatiquement votre adresse IPv4 globalement routable et crée un préfixe 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="45b36-121">Il effectue la configuration directement ou il peut écrire un script de configuration que vous pouvez inspecter et exécuter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="45b36-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="45b36-122">La syntaxe de la commande 6to4cfg.exe de base est la suivante.</span><span class="sxs-lookup"><span data-stu-id="45b36-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="45b36-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*extension*\]</span><span class="sxs-lookup"><span data-stu-id="45b36-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="45b36-124">Écrit le script de configuration dans un fichier, si vous spécifiez un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="45b36-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="45b36-125">Le script de configuration utilise Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="45b36-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="45b36-126">Vous pouvez spécifier con pour le nom de fichier pour écrire le script de configuration dans la sortie de la console, ce qui est utile pour voir ce que 6to4cfg.exe fera dans un scénario de test.</span><span class="sxs-lookup"><span data-stu-id="45b36-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="45b36-127">Si vous ne spécifiez pas de nom de fichier, 6to4cfg.exe met directement à jour la configuration IPv6 sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="45b36-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="45b36-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="45b36-129">Devient un routeur de passerelle 6to4 pour votre réseau local, ce qui permet le routage sur toutes vos interfaces et les préfixes de sous-réseau affectés.</span><span class="sxs-lookup"><span data-stu-id="45b36-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="45b36-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="45b36-131">Active l’adressage local du site dans votre site 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="45b36-132">Cette commande est utile uniquement lorsqu’elle est utilisée conjointement avec-r.</span><span class="sxs-lookup"><span data-stu-id="45b36-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="45b36-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="45b36-134">Spécifie que la configuration 6to4 doit être inversée.</span><span class="sxs-lookup"><span data-stu-id="45b36-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="45b36-135">Par conséquent, 6to4cfg-u inverse l’effet de 6to4cfg et 6to4cfg-r-u inverse l’effet de 6to4cfg-r, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="45b36-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*</span><span class="sxs-lookup"><span data-stu-id="45b36-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="45b36-137">Spécifie le nom ou l’adresse IPv4 d’un routeur relais 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="45b36-138">Le nom par défaut est 6to4.ipv6.microsoft.com, le routeur relais 6to4 sur Internet.</span><span class="sxs-lookup"><span data-stu-id="45b36-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="45b36-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="45b36-140">Spécifie que 6to4cfg.exe sélectionne la « meilleure » adresse de relais au lieu du premier.</span><span class="sxs-lookup"><span data-stu-id="45b36-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="45b36-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *adresse*</span><span class="sxs-lookup"><span data-stu-id="45b36-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="45b36-142">Spécifie l’adresse IPv4 locale pour le préfixe 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="45b36-143">Configuration 6to4 manuelle</span><span class="sxs-lookup"><span data-stu-id="45b36-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="45b36-144">Dans cet exemple, l’adresse de la passerelle 6to4 est 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="45b36-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="45b36-145">Vous avez besoin de votre propre adresse IPv4 globalement routable pour utiliser 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="45b36-146">L’adresse IP 172.31.42.239 est utilisée à titre d’exemple uniquement.</span><span class="sxs-lookup"><span data-stu-id="45b36-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="45b36-147">Il s’agit d’une adresse privée qui n’est pas routable globalement sur Internet.</span><span class="sxs-lookup"><span data-stu-id="45b36-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="45b36-148">L’adresse IPv4 à routage global 32 bits est combinée au préfixe 16 bits 2002 ::/16 pour former un préfixe d’adresse IPv6 de 48 bits pour votre site.</span><span class="sxs-lookup"><span data-stu-id="45b36-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="45b36-149">Dans cet exemple, le préfixe de site 6to4 est 2002 : ac1f : 2aef ::/48.</span><span class="sxs-lookup"><span data-stu-id="45b36-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="45b36-150">Notez que ac1f : 2aef est l’encodage hexadécimal de 172.31.42.239 (bien sûr, vous allez utiliser un préfixe différent basé sur votre propre adresse IPv4 routable globalement).</span><span class="sxs-lookup"><span data-stu-id="45b36-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="45b36-151">À l’aide du préfixe de site 6to4, vous pouvez affecter des adresses et des préfixes de sous-réseau à l’intérieur de votre site.</span><span class="sxs-lookup"><span data-stu-id="45b36-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="45b36-152">Cet exemple part du principe que vous utilisez le sous-réseau 0 pour configurer manuellement une adresse 6to4 sur votre ordinateur de passerelle 6to4 et que vous utilisez le sous-réseau 1 pour configurer automatiquement les adresses sur votre segment de réseau Ethernet.</span><span class="sxs-lookup"><span data-stu-id="45b36-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="45b36-153">Toutefois, d’autres options sont possibles.</span><span class="sxs-lookup"><span data-stu-id="45b36-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="45b36-154">Utilisez Ipv6.exe pour activer 6to4 sur votre ordinateur de passerelle 6to4 :</span><span class="sxs-lookup"><span data-stu-id="45b36-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="45b36-155">**RTU IPv6 2002 ::/16 2**</span><span class="sxs-lookup"><span data-stu-id="45b36-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="45b36-156">La commande **IPv6 RTU** effectue une mise à jour de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="45b36-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="45b36-157">Il peut être utilisé pour ajouter, supprimer ou mettre à jour un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="45b36-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="45b36-158">Dans ce cas, il active 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="45b36-159">L’argument 2002 ::/16 est le préfixe de l’itinéraire, en spécifiant le préfixe 6to4 unique.</span><span class="sxs-lookup"><span data-stu-id="45b36-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="45b36-160">L’argument 2 spécifie l’interface sur lien pour ce préfixe.</span><span class="sxs-lookup"><span data-stu-id="45b36-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="45b36-161">\#L’interface 2 est la « pseudo-interface » utilisée pour les tunnels configurés, le tunneling automatique et 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="45b36-162">Quand une adresse de destination IPv6 correspond au préfixe 2002 ::/16, les 32 bits qui suivent le préfixe dans l’adresse de destination sont extraits pour former une adresse de destination IPv4.</span><span class="sxs-lookup"><span data-stu-id="45b36-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="45b36-163">Le paquet est encapsulé avec un en-tête IPv4 et envoyé à l’adresse de destination IPv4.</span><span class="sxs-lookup"><span data-stu-id="45b36-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="45b36-164">Configurez une adresse 6to4 sur votre ordinateur de passerelle 6to4 :</span><span class="sxs-lookup"><span data-stu-id="45b36-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="45b36-165">**IPv6 Adu 2/2002 : ac1f : 2aef :: ac1f : 2aef**</span><span class="sxs-lookup"><span data-stu-id="45b36-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="45b36-166">La commande **IPv6 Adu** effectue une mise à jour d’adresse.</span><span class="sxs-lookup"><span data-stu-id="45b36-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="45b36-167">Il peut être utilisé pour ajouter, supprimer ou mettre à jour une adresse sur une interface.</span><span class="sxs-lookup"><span data-stu-id="45b36-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="45b36-168">Dans ce cas, il configure l’adresse 6to4 de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="45b36-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="45b36-169">L’argument 2/2002 : ac1f : 2aef :: ac1f : 2aef spécifie à la fois l’interface et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="45b36-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="45b36-170">Il requiert la configuration de l’adresse 2002 : ac1f : 2aef :: ac1f : 2aef sur l’interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="45b36-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="45b36-171">L’adresse est créée à l’aide du préfixe de site 2002 : ac1f : 2aef ::/48, sous-réseau 0 pour fournir un préfixe de sous-réseau : ac1f : 2aef ::/64 et un identificateur d’interface 64 bits.</span><span class="sxs-lookup"><span data-stu-id="45b36-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="45b36-172">La Convention présentée utilise l’adresse IPv4 de l’ordinateur pour l’identificateur d’interface pour les adresses affectées à l’interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="45b36-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="45b36-173">Pour votre utilisation, ac1f : 2aef doit être remplacé par le codage hexadécimal de votre propre adresse IPv4 routable globalement.</span><span class="sxs-lookup"><span data-stu-id="45b36-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="45b36-174">Les deux commandes précédentes sont suffisantes pour permettre la communication avec d’autres sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="45b36-175">Par exemple, vous pouvez essayer d’exécuter une commande ping sur le site Microsoft 6to4 :</span><span class="sxs-lookup"><span data-stu-id="45b36-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="45b36-176">**ping6 2002:836b : 9820 :: 836b : 9820**</span><span class="sxs-lookup"><span data-stu-id="45b36-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="45b36-177">Pour activer la communication avec 6bone, vous devez créer un tunnel configuré par défaut vers un relais 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="45b36-178">Vous pouvez utiliser le routeur Microsoft 6to4 Relay, 131.107.152.32 :</span><span class="sxs-lookup"><span data-stu-id="45b36-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="45b36-179">**RTU IPv6 ::/0 2/ :: 131.107.152.32 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="45b36-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="45b36-180">La commande **IPv6 RTU** effectue une mise à jour de la table de routage, en établissant, dans cette instance, un itinéraire par défaut vers le relais 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="45b36-181">L’argument ::/0 est le préfixe d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="45b36-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="45b36-182">Le préfixe de longueur zéro indique qu’il s’agit d’un itinéraire par défaut.</span><span class="sxs-lookup"><span data-stu-id="45b36-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="45b36-183">L’argument 2/ :: 131.107.152.32 spécifie le voisin de saut suivant pour ce préfixe.</span><span class="sxs-lookup"><span data-stu-id="45b36-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="45b36-184">Elle nécessite que les paquets correspondant au préfixe soient transmis à address :: 131.107.152.32 à l’aide de l’interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="45b36-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="45b36-185">Le transfert d’un paquet vers :: 131.107.152.32 sur l’interface \# 2 provoque l’encapsulation d’un paquet avec un en-tête V4 et son envoi à 131.107.152.32.</span><span class="sxs-lookup"><span data-stu-id="45b36-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="45b36-186">L’argument pub rend cet itinéraire publié.</span><span class="sxs-lookup"><span data-stu-id="45b36-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="45b36-187">Étant donné que cela ne concerne que les routeurs, il n’a aucun effet tant que le routage n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="45b36-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="45b36-188">De même, la durée de vie de 30 minutes concerne uniquement si le routage est activé.</span><span class="sxs-lookup"><span data-stu-id="45b36-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="45b36-189">Vous devez être en mesure d’accéder aux sites 6bone et aux sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="45b36-190">Pour tester cela, vous pouvez utiliser la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="45b36-190">You can use the following command to test this:</span></span>

<span data-ttu-id="45b36-191">**ping6 3FFE : 1cff : 0 : F5 :: 1**</span><span class="sxs-lookup"><span data-stu-id="45b36-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="45b36-192">La dernière étape consiste à activer le routage sur votre passerelle 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="45b36-193">Cet exemple suppose que l’interface \# 3 sur votre ordinateur de passerelle est une interface Ethernet et que l’interface \# 4 est 6-sur-4.</span><span class="sxs-lookup"><span data-stu-id="45b36-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="45b36-194">Votre ordinateur peut numéroter ses interfaces différemment.</span><span class="sxs-lookup"><span data-stu-id="45b36-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="45b36-195">Les deux commandes suivantes affectent des préfixes de sous-réseau aux deux liens.</span><span class="sxs-lookup"><span data-stu-id="45b36-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="45b36-196">Les préfixes de sous-réseau sont dérivés du préfixe 6to4 de site 2002 : ac1f : 2aef ::/48 :</span><span class="sxs-lookup"><span data-stu-id="45b36-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="45b36-197">**IPv6 RTU 2002 : ac1f : 2aef : 1 ::/64 3 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="45b36-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="45b36-198">**IPv6 RTU 2002 : ac1f : 2aef : 2 ::/64 4 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="45b36-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="45b36-199">La commande **IPv6 RTU** spécifie que le préfixe 2002 : ac1f : 2aef : 1 ::/64 est sur liaison avec l’interface \# 3.</span><span class="sxs-lookup"><span data-stu-id="45b36-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="45b36-200">Il configure le premier préfixe de sous-réseau sur l’interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="45b36-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="45b36-201">L’itinéraire est publié avec une durée de vie de 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="45b36-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="45b36-202">De même, le préfixe 2002 : ac1f : 2aef : 2 ::/64 est configuré sur l’interface 6-sur-4.</span><span class="sxs-lookup"><span data-stu-id="45b36-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="45b36-203">Les trois commandes suivantes permettent à l’ordinateur de passerelle 6to4 de fonctionner en tant que routeur :</span><span class="sxs-lookup"><span data-stu-id="45b36-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="45b36-204">**FORW IPv6 IFC 2**</span><span class="sxs-lookup"><span data-stu-id="45b36-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="45b36-205">**IPv6 IFC 3 FORW ADV**</span><span class="sxs-lookup"><span data-stu-id="45b36-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="45b36-206">**IFC IPv6 FORW ADV**</span><span class="sxs-lookup"><span data-stu-id="45b36-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="45b36-207">La commande **IPv6 IFC** contrôle les attributs d’une interface.</span><span class="sxs-lookup"><span data-stu-id="45b36-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="45b36-208">Un routeur transfère les paquets et envoie les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="45b36-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="45b36-209">Dans l’implémentation Microsoft IPv6, ces attributs par interface sont contrôlés séparément.</span><span class="sxs-lookup"><span data-stu-id="45b36-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="45b36-210">L’interface \# 2 n’est pas nécessaire pour la publication, car il s’agit d’une pseudo-interface.</span><span class="sxs-lookup"><span data-stu-id="45b36-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="45b36-211">Si votre ordinateur possède des interfaces supplémentaires, celles-ci doivent également être configurées pour le transfert et la publication.</span><span class="sxs-lookup"><span data-stu-id="45b36-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="45b36-212">Après l’exécution de ces commandes, le protocole IPv6 de Microsoft configure automatiquement les adresses sur \# les interfaces 3 et \# 4 à l’aide des préfixes de sous-réseau respectifs et les deux interfaces commencent à envoyer des publications de routeur entre 3 et 10 minutes environ.</span><span class="sxs-lookup"><span data-stu-id="45b36-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="45b36-213">Les hôtes recevant ces annonces de routeur se configurent automatiquement avec un itinéraire par défaut et une adresse 6to4 dérivée du préfixe de sous-réseau de leur lien.</span><span class="sxs-lookup"><span data-stu-id="45b36-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="45b36-214">Ils auront une communication avec d’autres sites 6to4 et le 6bone via l’ordinateur passerelle.</span><span class="sxs-lookup"><span data-stu-id="45b36-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="45b36-215">Débogage de la configuration 6to4</span><span class="sxs-lookup"><span data-stu-id="45b36-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="45b36-216">**Pour déboguer votre configuration 6to4**</span><span class="sxs-lookup"><span data-stu-id="45b36-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="45b36-217">Vérifiez votre connectivité IPv4 au routeur relais 6to4 :</span><span class="sxs-lookup"><span data-stu-id="45b36-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="45b36-218">**ping 6to4.ipv6.microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="45b36-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="45b36-219">En cas d’échec, vous ne disposez pas d’une connectivité Internet globale.</span><span class="sxs-lookup"><span data-stu-id="45b36-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="45b36-220">Vérifiez l’encapsulation IPv6 à l’aide du tunneling automatique :</span><span class="sxs-lookup"><span data-stu-id="45b36-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="45b36-221">**ping6 :: 131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="45b36-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="45b36-222">En cas d’échec, vous pouvez avoir un pare-feu ou un traducteur d’adresses réseau (NAT) entre votre ordinateur et Internet.</span><span class="sxs-lookup"><span data-stu-id="45b36-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="45b36-223">Si cette opération réussit, votre connexion Internet peut prendre en charge 6to4.</span><span class="sxs-lookup"><span data-stu-id="45b36-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="45b36-224">Vérifiez l’affichage de la commande IPv6 RT.</span><span class="sxs-lookup"><span data-stu-id="45b36-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="45b36-225">Un itinéraire 2002 ::/16-> 2 doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="45b36-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="45b36-226">Vérifiez l’affichage de la commande IPv6 si 2.</span><span class="sxs-lookup"><span data-stu-id="45b36-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="45b36-227">Vous devez voir une adresse par défaut avec un préfixe 2002 ::/16.</span><span class="sxs-lookup"><span data-stu-id="45b36-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="45b36-228">L’adresse IPv4 du routeur de relais Microsoft 6to4 de 131.107.152.32 est susceptible d’être modifiée.</span><span class="sxs-lookup"><span data-stu-id="45b36-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="45b36-229">Si l’étape 2 ci-dessus ne fonctionne pas, vérifiez la sortie de la commande ping à l’étape 1 pour vérifier l’adresse IPv4 du routeur Microsoft 6to4 Relay.</span><span class="sxs-lookup"><span data-stu-id="45b36-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="45b36-230">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45b36-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45b36-231">Configurations recommandées pour IPv6</span><span class="sxs-lookup"><span data-stu-id="45b36-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="45b36-232">Sous-réseau unique avec adresses lien-local</span><span class="sxs-lookup"><span data-stu-id="45b36-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="45b36-233">Utilisation d’IPsec entre deux hôtes de liaison locale</span><span class="sxs-lookup"><span data-stu-id="45b36-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



