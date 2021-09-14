---
description: Le fournisseur d’itinéraires IP WMI et les classes de réseau fournissent des données pour les adresses IPv4. depuis Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Prise en charge D’ipv6 et IPv6 dans WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010455"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Prise en charge D’ipv6 et IPv6 dans WMI

Le [fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI et les classes de réseau fournissent des données pour les adresses IPv4. depuis Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.

## <a name="wmi-ip-data"></a>Données IP WMI

Les classes suivantes fournissent uniquement des données IPv4 :

-   [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**\_ActiveRoute Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**\_NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Les classes suivantes fournissent des données pour IPv4 et IPv6.

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    La propriété **IpAddess** contient l’adresse IPv6 de l’ordinateur dans un réseau IPv6.

-   [**\_PingStatus Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) peut retourner des données pour les adresses IPv4 ou IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Connexions IPv4 et IPv6 à WMI

Lors de la connexion à un espace de noms WMI sur un ordinateur distant, l’ordinateur cible doit exécuter le même logiciel IP que l’ordinateur qui se connecte. Par exemple, un ordinateur exécutant IPv4 ne peut pas se connecter à un ordinateur exécutant IPv6, même si la connexion est tentée à l’aide d’un nom d’ordinateur dans l’appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), ou en utilisant la `winmgmts` connexion moniker. L’inverse est également vrai : un ordinateur exécutant uniquement IPv6 ne peut pas se connecter à un ordinateur exécutant uniquement IPv4.

Si l’ordinateur cible exécute à la fois IPv4 et IPv6, une connexion peut être établie à partir d’un ordinateur exécutant l’un des logiciels IP. Un nom d’ordinateur ou une adresse IP au format IPv4 ou IPv6 peut être fourni dans la connexion à un espace de noms WMI.

Un ordinateur qui exécute à la fois IPv4 et IPv6 et se connecte à un ordinateur cible qui exécute uniquement IPv4 ou IPv6 doit fournir une adresse IP au format approprié pour le logiciel IP de l’ordinateur cible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 
