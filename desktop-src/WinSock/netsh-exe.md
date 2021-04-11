---
description: Les commandes netsh pour IPv6 fournissent un outil en ligne de commande que vous pouvez utiliser pour interroger et configurer des interfaces, des adresses, des caches et des itinéraires IPv6. Les commandes netsh interface IPv6 sont prises en charge sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113030"
---
# <a name="netshexe"></a><span data-ttu-id="7c0f6-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="7c0f6-104">Netsh.exe</span></span>

<span data-ttu-id="7c0f6-105">Les commandes netsh pour IPv6 fournissent un outil en ligne de commande que vous pouvez utiliser pour interroger et configurer des interfaces, des adresses, des caches et des itinéraires IPv6.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="7c0f6-106">Les commandes netsh interface IPv6 sont prises en charge sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="7c0f6-107">Netsh.exe possède de nombreuses sous-commandes pour IPv6.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="7c0f6-108">La liste complète des options pour netsh interface IPv6 est disponible à partir de l’invite de commandes sur Windows XP avec SP1 et versions ultérieures en tapant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7c0f6-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="7c0f6-109">**netsh interface IPv6/ ?**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="7c0f6-110">La documentation sur toutes les commandes **netsh** pour IPv6 est également disponible en ligne sur TechNet.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="7c0f6-111">Pour plus d’informations sur **netsh** sur Windows Server 2008, consultez [commandes netsh pour l’interface (IPv4 et IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c0f6-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="7c0f6-112">Pour plus d’informations sur **netsh** sur Windows Server 2003, consultez [commandes netsh pour l’interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="7c0f6-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="7c0f6-113">Voici quelques-unes des commandes couramment utilisées pour IPv6, bien que de nombreuses autres commandes soient prises en charge :</span><span class="sxs-lookup"><span data-stu-id="7c0f6-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="7c0f6-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface IPv6 Add Address**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-115">Ajoute une adresse IPv6 à une interface spécifique sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="7c0f6-116">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface IPv6 Add DNS**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-118">Ajoute une adresse IPv6 de serveur DNS à la liste de serveurs DNS configurée de manière statique pour l’interface spécifiée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="7c0f6-119">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-121">Ajoute un itinéraire pour une adresse de préfixe IPv6 spécifiée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="7c0f6-122">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**adresse netsh de l’interface IPv6 Delete**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-124">Supprime l’adresse IPv6 spécifiée d’une interface spécifique sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="7c0f6-125">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-127">Supprime une adresse de serveur DNS de la liste de serveurs DNS configurée de manière statique pour l’interface spécifiée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="7c0f6-128">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface IPv6 Delete interface**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-130">Supprime une interface spécifiée de la pile IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="7c0f6-131">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface IPv6 Delete route**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-133">Supprime un itinéraire pour une adresse de préfixe IPv6 spécifiée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="7c0f6-134">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**vidage IPv6 de l’interface netsh**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-136">Crée un script qui contient les commandes permettant de créer la configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="7c0f6-137">S’il est enregistré dans un fichier, ce script peut être utilisé pour restaurer les paramètres de configuration modifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**installation de netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-139">Installe le protocole IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface IPv6 renouvelé**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-141">Redémarre les interfaces IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**réinitialisation IPv6 de l’interface netsh**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-143">Réinitialise l’état de configuration IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-145">Affiche les paramètres de configuration globale pour IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-147">Affiche toutes les adresses IPv6 ou toutes les adresses IPv6 sur une interface spécifique sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="7c0f6-148">Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c0f6-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**désinstallation de netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-150">Désinstalle le protocole IPv6 sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="7c0f6-151">Commandes netsh pour IPv4</span><span class="sxs-lookup"><span data-stu-id="7c0f6-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="7c0f6-152">Des commandes netsh similaires sont disponibles pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="7c0f6-153">La liste complète des options pour les commandes netsh à utiliser avec IPv4 est disponible à partir de l’invite de commandes sur Windows XP avec SP1 et versions ultérieures en tapant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7c0f6-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="7c0f6-154">**netsh interface IP/ ?**</span><span class="sxs-lookup"><span data-stu-id="7c0f6-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="7c0f6-155">La documentation sur toutes les commandes netsh pour IPv4 est également disponible en ligne sur TechNet.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="7c0f6-156">Pour plus d’informations, consultez [commandes netsh pour l’interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="7c0f6-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
