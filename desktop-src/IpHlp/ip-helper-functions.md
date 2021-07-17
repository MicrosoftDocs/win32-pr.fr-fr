---
title: Fonctions d’assistance IP
description: Les fonctions suivantes récupèrent et modifient les paramètres de configuration pour le transport TCP/IP sur l’ordinateur local.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ee16bb0b65545c4abbef387c5b90d42fb9d3c629
ms.sourcegitcommit: ea0069adb72dbfa717e73f3a96c3407a49ec0dab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2021
ms.locfileid: "114394209"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="63464-103">Fonctions d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="63464-103">IP Helper functions</span></span>

<span data-ttu-id="63464-104">Les fonctions suivantes récupèrent et modifient les paramètres de configuration pour le transport TCP/IP sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="63464-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="63464-105">La liste catégorique suivante peut aider à déterminer la collection de fonctions qui convient le mieux à une tâche donnée.</span><span class="sxs-lookup"><span data-stu-id="63464-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="63464-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="63464-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="63464-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="63464-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="63464-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="63464-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="63464-109">Gestion des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="63464-109">Adapter management</span></span>

-   [<span data-ttu-id="63464-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="63464-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="63464-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="63464-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="63464-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="63464-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="63464-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="63464-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="63464-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="63464-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="63464-115">Gestion ARP (Address Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="63464-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="63464-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="63464-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="63464-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="63464-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="63464-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="63464-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="63464-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="63464-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="63464-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="63464-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="63464-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="63464-124">Conversion de l’interface</span><span class="sxs-lookup"><span data-stu-id="63464-124">Interface conversion</span></span>

-   [<span data-ttu-id="63464-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="63464-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="63464-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="63464-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="63464-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="63464-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="63464-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="63464-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="63464-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="63464-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="63464-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="63464-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="63464-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="63464-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="63464-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="63464-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="63464-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="63464-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="63464-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="63464-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="63464-135">**Si \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="63464-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="63464-136">**Si \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="63464-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="63464-137">Gestion des interfaces</span><span class="sxs-lookup"><span data-stu-id="63464-137">Interface management</span></span>

-   [<span data-ttu-id="63464-138">**FreeInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="63464-138">**FreeInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-freeinterfacednssettings)
-   [<span data-ttu-id="63464-139">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="63464-139">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="63464-140">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-140">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="63464-141">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-141">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="63464-142">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="63464-142">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="63464-143">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="63464-143">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="63464-144">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="63464-144">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="63464-145">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="63464-145">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="63464-146">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="63464-146">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="63464-147">**GetInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="63464-147">**GetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
-   [<span data-ttu-id="63464-148">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="63464-148">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="63464-149">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="63464-149">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="63464-150">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-150">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="63464-151">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="63464-151">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="63464-152">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="63464-152">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="63464-153">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-153">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="63464-154">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-154">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="63464-155">**SetInterfaceDnsSettings**</span><span class="sxs-lookup"><span data-stu-id="63464-155">**SetInterfaceDnsSettings**</span></span>](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
-   [<span data-ttu-id="63464-156">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-156">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="63464-157">Protocole Internet (IP) et protocole ICMP (Internet Control Message Protocol)</span><span class="sxs-lookup"><span data-stu-id="63464-157">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="63464-158">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="63464-158">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="63464-159">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="63464-159">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="63464-160">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="63464-160">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="63464-161">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="63464-161">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="63464-162">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="63464-162">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="63464-163">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="63464-163">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="63464-164">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="63464-164">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="63464-165">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="63464-165">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="63464-166">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="63464-166">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="63464-167">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="63464-167">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="63464-168">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="63464-168">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="63464-169">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="63464-169">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="63464-170">Gestion des adresses IP</span><span class="sxs-lookup"><span data-stu-id="63464-170">IP address management</span></span>

-   [<span data-ttu-id="63464-171">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-171">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="63464-172">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-172">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="63464-173">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-173">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="63464-174">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-174">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="63464-175">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-175">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="63464-176">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-176">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="63464-177">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-177">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="63464-178">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="63464-178">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="63464-179">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="63464-179">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="63464-180">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-180">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="63464-181">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="63464-181">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="63464-182">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-182">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="63464-183">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="63464-183">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="63464-184">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-184">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="63464-185">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-185">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="63464-186">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-186">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="63464-187">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="63464-187">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="63464-188">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-188">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="63464-189">Conversion de chaîne d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="63464-189">IP address string conversion</span></span>

-   [<span data-ttu-id="63464-190">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="63464-190">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="63464-191">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="63464-191">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="63464-192">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-192">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="63464-193">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="63464-193">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="63464-194">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="63464-194">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="63464-195">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="63464-195">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="63464-196">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="63464-196">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="63464-197">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="63464-197">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="63464-198">Gestion des adresses IP voisines</span><span class="sxs-lookup"><span data-stu-id="63464-198">IP neighbor address management</span></span>

-   [<span data-ttu-id="63464-199">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-199">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="63464-200">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-200">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="63464-201">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="63464-201">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="63464-202">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-202">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="63464-203">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="63464-203">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="63464-204">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-204">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="63464-205">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="63464-205">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="63464-206">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-206">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="63464-207">Gestion des chemins d’accès IP</span><span class="sxs-lookup"><span data-stu-id="63464-207">IP path management</span></span>

-   [<span data-ttu-id="63464-208">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="63464-208">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="63464-209">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-209">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="63464-210">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="63464-210">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="63464-211">Gestion des itinéraires IP</span><span class="sxs-lookup"><span data-stu-id="63464-211">IP route management</span></span>

-   [<span data-ttu-id="63464-212">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-212">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="63464-213">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-213">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="63464-214">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-214">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="63464-215">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-215">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="63464-216">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="63464-216">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="63464-217">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="63464-217">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="63464-218">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="63464-218">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="63464-219">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="63464-219">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="63464-220">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="63464-220">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="63464-221">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-221">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="63464-222">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="63464-222">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="63464-223">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="63464-223">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="63464-224">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="63464-224">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="63464-225">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-225">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="63464-226">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-226">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="63464-227">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="63464-227">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="63464-228">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="63464-228">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="63464-229">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="63464-229">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="63464-230">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="63464-230">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="63464-231">Gestion de la mémoire de la table IP</span><span class="sxs-lookup"><span data-stu-id="63464-231">IP table memory management</span></span>

-   [<span data-ttu-id="63464-232">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="63464-232">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="63464-233">Utilitaire IP</span><span class="sxs-lookup"><span data-stu-id="63464-233">IP utility</span></span>

-   [<span data-ttu-id="63464-234">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="63464-234">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="63464-235">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="63464-235">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="63464-236">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="63464-236">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="63464-237">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="63464-237">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="63464-238">Configuration réseau</span><span class="sxs-lookup"><span data-stu-id="63464-238">Network configuration</span></span>

-   [<span data-ttu-id="63464-239">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="63464-239">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="63464-240">Notification</span><span class="sxs-lookup"><span data-stu-id="63464-240">Notification</span></span>

-   [<span data-ttu-id="63464-241">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="63464-241">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="63464-242">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="63464-242">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="63464-243">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="63464-243">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="63464-244">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="63464-244">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="63464-245">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="63464-245">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="63464-246">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="63464-246">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="63464-247">Horodatage des paquets</span><span class="sxs-lookup"><span data-stu-id="63464-247">Packet timestamping</span></span>

-   [<span data-ttu-id="63464-248">**CaptureInterfaceHardwareCrossTimestamp**</span><span class="sxs-lookup"><span data-stu-id="63464-248">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="63464-249">**GetInterfaceActiveTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="63464-249">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="63464-250">**GetInterfaceSupportedTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="63464-250">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="63464-251">**RegisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="63464-251">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="63464-252">**UnregisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="63464-252">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="63464-253">Réservation de port persistant</span><span class="sxs-lookup"><span data-stu-id="63464-253">Persistent port reservation</span></span>

-   [<span data-ttu-id="63464-254">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-254">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="63464-255">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-255">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="63464-256">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-256">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="63464-257">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-257">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="63464-258">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-258">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="63464-259">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="63464-259">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="63464-260">Intégrité de la sécurité</span><span class="sxs-lookup"><span data-stu-id="63464-260">Security health</span></span>

-   <span data-ttu-id="63464-261">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63464-261">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="63464-262">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63464-262">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="63464-263">ces fonctions sont définies uniquement sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="63464-263">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="63464-264">ces fonctions ne sont pas disponibles sur Windows Vista, ni sur Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="63464-264">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="63464-265">Gestion du client IPv6 Teredo</span><span class="sxs-lookup"><span data-stu-id="63464-265">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="63464-266">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="63464-266">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="63464-267">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="63464-267">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="63464-268">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="63464-268">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="63464-269">Protocole TCP (Transmission Control Protocol) et UDP (User Datagram Protocol)</span><span class="sxs-lookup"><span data-stu-id="63464-269">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="63464-270">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="63464-270">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="63464-271">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="63464-271">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="63464-272">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="63464-272">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="63464-273">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-273">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="63464-274">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="63464-274">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="63464-275">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-275">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="63464-276">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="63464-276">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="63464-277">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="63464-277">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="63464-278">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="63464-278">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="63464-279">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="63464-279">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="63464-280">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="63464-280">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="63464-281">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="63464-281">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="63464-282">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="63464-282">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="63464-283">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="63464-283">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="63464-284">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="63464-284">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="63464-285">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="63464-285">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="63464-286">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="63464-286">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="63464-287">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="63464-287">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="63464-288">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="63464-288">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="63464-289">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="63464-289">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="63464-290">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="63464-290">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="63464-291">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="63464-291">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="63464-292">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="63464-292">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="63464-293">API déconseillées</span><span class="sxs-lookup"><span data-stu-id="63464-293">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="63464-294">Ces fonctions sont dépréciées et ne sont pas prises en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63464-294">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="63464-295">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="63464-295">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="63464-296">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="63464-296">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
