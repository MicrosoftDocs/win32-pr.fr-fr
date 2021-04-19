---
description: Le fournisseur d’itinéraires IP WMI et les classes de réseau fournissent des données pour les adresses IPv4. À compter de Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Prise en charge D’ipv6 et IPv6 dans WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521287"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="bff2f-104">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="bff2f-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="bff2f-105">Le [fournisseur d’itinéraires IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI et les classes de réseau fournissent des données pour les adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="bff2f-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="bff2f-106">À compter de Windows Vista, WMI fournit également une prise en charge limitée des fonctionnalités de réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="bff2f-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="bff2f-107">Données IP WMI</span><span class="sxs-lookup"><span data-stu-id="bff2f-107">WMI IP Data</span></span>

<span data-ttu-id="bff2f-108">Les classes suivantes fournissent uniquement des données IPv4 :</span><span class="sxs-lookup"><span data-stu-id="bff2f-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="bff2f-109">**\_IP4RouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="bff2f-110">**\_IP4PersistedRouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="bff2f-111">**\_IP4RouteTableEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="bff2f-112">**\_ActiveRoute Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="bff2f-113">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="bff2f-114">Les classes suivantes fournissent des données pour IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="bff2f-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="bff2f-115">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="bff2f-116">La propriété **IpAddess** contient l’adresse IPv6 de l’ordinateur dans un réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="bff2f-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="bff2f-117">**\_PingStatus Win32**</span><span class="sxs-lookup"><span data-stu-id="bff2f-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="bff2f-118">[**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) peut retourner des données pour les adresses IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="bff2f-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="bff2f-119">Connexions IPv4 et IPv6 à WMI</span><span class="sxs-lookup"><span data-stu-id="bff2f-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="bff2f-120">Lors de la connexion à un espace de noms WMI sur un ordinateur distant, l’ordinateur cible doit exécuter le même logiciel IP que l’ordinateur qui se connecte.</span><span class="sxs-lookup"><span data-stu-id="bff2f-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="bff2f-121">Par exemple, un ordinateur exécutant IPv4 ne peut pas se connecter à un ordinateur exécutant IPv6, même si la connexion est tentée à l’aide d’un nom d’ordinateur dans l’appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), ou en utilisant la `winmgmts` connexion moniker.</span><span class="sxs-lookup"><span data-stu-id="bff2f-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="bff2f-122">L’inverse est également vrai : un ordinateur exécutant uniquement IPv6 ne peut pas se connecter à un ordinateur exécutant uniquement IPv4.</span><span class="sxs-lookup"><span data-stu-id="bff2f-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="bff2f-123">Si l’ordinateur cible exécute à la fois IPv4 et IPv6, une connexion peut être établie à partir d’un ordinateur exécutant l’un des logiciels IP.</span><span class="sxs-lookup"><span data-stu-id="bff2f-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="bff2f-124">Un nom d’ordinateur ou une adresse IP au format IPv4 ou IPv6 peut être fourni dans la connexion à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="bff2f-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="bff2f-125">Un ordinateur qui exécute à la fois IPv4 et IPv6 et se connecte à un ordinateur cible qui exécute uniquement IPv4 ou IPv6 doit fournir une adresse IP au format approprié pour le logiciel IP de l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="bff2f-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bff2f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bff2f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bff2f-127">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="bff2f-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
