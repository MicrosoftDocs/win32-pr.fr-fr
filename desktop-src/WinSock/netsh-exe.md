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
# <a name="netshexe"></a>Netsh.exe

Les commandes netsh pour IPv6 fournissent un outil en ligne de commande que vous pouvez utiliser pour interroger et configurer des interfaces, des adresses, des caches et des itinéraires IPv6. Les commandes netsh interface IPv6 sont prises en charge sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures.

Netsh.exe possède de nombreuses sous-commandes pour IPv6. La liste complète des options pour netsh interface IPv6 est disponible à partir de l’invite de commandes sur Windows XP avec SP1 et versions ultérieures en tapant ce qui suit :

**netsh interface IPv6/ ?**

La documentation sur toutes les commandes **netsh** pour IPv6 est également disponible en ligne sur TechNet. Pour plus d’informations sur **netsh** sur Windows Server 2008, consultez [commandes netsh pour l’interface (IPv4 et IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)). Pour plus d’informations sur **netsh** sur Windows Server 2003, consultez [commandes netsh pour l’interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).

Voici quelques-unes des commandes couramment utilisées pour IPv6, bien que de nombreuses autres commandes soient prises en charge :

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface IPv6 Add Address**
</dt> <dd>

Ajoute une adresse IPv6 à une interface spécifique sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface IPv6 Add DNS**
</dt> <dd>

Ajoute une adresse IPv6 de serveur DNS à la liste de serveurs DNS configurée de manière statique pour l’interface spécifiée sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**
</dt> <dd>

Ajoute un itinéraire pour une adresse de préfixe IPv6 spécifiée sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**adresse netsh de l’interface IPv6 Delete**
</dt> <dd>

Supprime l’adresse IPv6 spécifiée d’une interface spécifique sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**
</dt> <dd>

Supprime une adresse de serveur DNS de la liste de serveurs DNS configurée de manière statique pour l’interface spécifiée sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface IPv6 Delete interface**
</dt> <dd>

Supprime une interface spécifiée de la pile IPv6 sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface IPv6 Delete route**
</dt> <dd>

Supprime un itinéraire pour une adresse de préfixe IPv6 spécifiée sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**vidage IPv6 de l’interface netsh**
</dt> <dd>

Crée un script qui contient les commandes permettant de créer la configuration actuelle. S’il est enregistré dans un fichier, ce script peut être utilisé pour restaurer les paramètres de configuration modifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**installation de netsh interface IPv6**
</dt> <dd>

Installe le protocole IPv6 sur l’ordinateur local.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface IPv6 renouvelé**
</dt> <dd>

Redémarre les interfaces IPv6 sur l’ordinateur local.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**réinitialisation IPv6 de l’interface netsh**
</dt> <dd>

Réinitialise l’état de configuration IPv6 sur l’ordinateur local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**
</dt> <dd>

Affiche les paramètres de configuration globale pour IPv6 sur l’ordinateur local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**
</dt> <dd>

Affiche toutes les adresses IPv6 ou toutes les adresses IPv6 sur une interface spécifique sur l’ordinateur local. Cette commande comporte des paramètres de sous-options qui doivent être spécifiés.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**désinstallation de netsh interface IPv6**
</dt> <dd>

Désinstalle le protocole IPv6 sur l’ordinateur local.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Commandes netsh pour IPv4

Des commandes netsh similaires sont disponibles pour IPv4. La liste complète des options pour les commandes netsh à utiliser avec IPv4 est disponible à partir de l’invite de commandes sur Windows XP avec SP1 et versions ultérieures en tapant ce qui suit :

**netsh interface IP/ ?**

La documentation sur toutes les commandes netsh pour IPv4 est également disponible en ligne sur TechNet. Pour plus d’informations, consultez [commandes netsh pour l’interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))

 

 
