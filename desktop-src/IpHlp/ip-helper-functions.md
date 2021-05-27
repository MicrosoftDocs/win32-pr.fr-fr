---
title: Fonctions d’assistance IP
description: Les fonctions suivantes récupèrent et modifient les paramètres de configuration pour le transport TCP/IP sur l’ordinateur local.
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
ms.openlocfilehash: ae19803c25512242b613735a060c7beda8c1df70
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549504"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="bd193-103">Fonctions d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="bd193-103">IP Helper functions</span></span>

<span data-ttu-id="bd193-104">Les fonctions suivantes récupèrent et modifient les paramètres de configuration pour le transport TCP/IP sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd193-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="bd193-105">La liste catégorique suivante peut aider à déterminer la collection de fonctions qui convient le mieux à une tâche donnée.</span><span class="sxs-lookup"><span data-stu-id="bd193-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="bd193-106">**GetNetworkConnectivityHint**</span><span class="sxs-lookup"><span data-stu-id="bd193-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="bd193-107">**GetNetworkConnectivityHintForInterface**</span><span class="sxs-lookup"><span data-stu-id="bd193-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="bd193-108">**NotifyNetworkConnectivityHintChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="bd193-109">Gestion des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="bd193-109">Adapter management</span></span>

-   [<span data-ttu-id="bd193-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="bd193-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="bd193-111">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="bd193-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="bd193-112">**GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="bd193-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="bd193-113">**GetPerAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="bd193-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="bd193-114">**GetUniDirectionalAdapterInfo**</span><span class="sxs-lookup"><span data-stu-id="bd193-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="bd193-115">Gestion ARP (Address Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="bd193-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="bd193-116">**CreateIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="bd193-117">**CreateProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="bd193-118">**DeleteIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="bd193-119">**DeleteProxyArpEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="bd193-120">**FlushIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="bd193-121">**GetIpNetTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="bd193-122">**SendARP**</span><span class="sxs-lookup"><span data-stu-id="bd193-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="bd193-123">**SetIpNetEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="bd193-124">Conversion de l’interface</span><span class="sxs-lookup"><span data-stu-id="bd193-124">Interface conversion</span></span>

-   [<span data-ttu-id="bd193-125">**ConvertInterfaceAliasToLuid**</span><span class="sxs-lookup"><span data-stu-id="bd193-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="bd193-126">**ConvertInterfaceGuidToLuid**</span><span class="sxs-lookup"><span data-stu-id="bd193-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="bd193-127">**ConvertInterfaceIndexToLuid**</span><span class="sxs-lookup"><span data-stu-id="bd193-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="bd193-128">**ConvertInterfaceLuidToAlias**</span><span class="sxs-lookup"><span data-stu-id="bd193-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="bd193-129">**ConvertInterfaceLuidToGuid**</span><span class="sxs-lookup"><span data-stu-id="bd193-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="bd193-130">**ConvertInterfaceLuidToIndex**</span><span class="sxs-lookup"><span data-stu-id="bd193-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="bd193-131">**ConvertInterfaceLuidToNameA**</span><span class="sxs-lookup"><span data-stu-id="bd193-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="bd193-132">**ConvertInterfaceLuidToNameW**</span><span class="sxs-lookup"><span data-stu-id="bd193-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="bd193-133">**ConvertInterfaceNameToLuidA**</span><span class="sxs-lookup"><span data-stu-id="bd193-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="bd193-134">**ConvertInterfaceNameToLuidW**</span><span class="sxs-lookup"><span data-stu-id="bd193-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="bd193-135">**Si \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="bd193-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="bd193-136">**Si \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="bd193-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="bd193-137">Gestion des interfaces</span><span class="sxs-lookup"><span data-stu-id="bd193-137">Interface management</span></span>

-   [<span data-ttu-id="bd193-138">**GetFriendlyIfIndex**</span><span class="sxs-lookup"><span data-stu-id="bd193-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="bd193-139">**GetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="bd193-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="bd193-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="bd193-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="bd193-142">**GetIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="bd193-143">**GetIfTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="bd193-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="bd193-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="bd193-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="bd193-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="bd193-146">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="bd193-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="bd193-147">**GetInvertedIfStackTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="bd193-148">**GetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="bd193-149">**GetIpInterfaceTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="bd193-150">**GetNumberOfInterfaces**</span><span class="sxs-lookup"><span data-stu-id="bd193-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="bd193-151">**InitializeIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="bd193-152">**SetIfEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="bd193-153">**SetIpInterfaceEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="bd193-154">Protocole Internet (IP) et protocole ICMP (Internet Control Message Protocol)</span><span class="sxs-lookup"><span data-stu-id="bd193-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="bd193-155">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="bd193-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="bd193-156">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="bd193-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="bd193-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="bd193-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="bd193-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="bd193-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="bd193-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="bd193-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="bd193-160">**IcmpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="bd193-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="bd193-161">**IcmpCreateFile**</span><span class="sxs-lookup"><span data-stu-id="bd193-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="bd193-162">**IcmpParseReplies**</span><span class="sxs-lookup"><span data-stu-id="bd193-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="bd193-163">**IcmpSendEcho**</span><span class="sxs-lookup"><span data-stu-id="bd193-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="bd193-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="bd193-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="bd193-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="bd193-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="bd193-166">**SetIpTTL**</span><span class="sxs-lookup"><span data-stu-id="bd193-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="bd193-167">Gestion des adresses IP</span><span class="sxs-lookup"><span data-stu-id="bd193-167">IP address management</span></span>

-   [<span data-ttu-id="bd193-168">**AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="bd193-169">**CreateAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="bd193-170">**CreateUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="bd193-171">**DeleteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="bd193-172">**DeleteAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="bd193-173">**DeleteUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="bd193-174">**GetAnycastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="bd193-175">**GetAnycastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="bd193-176">**GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="bd193-177">**GetMulticastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="bd193-178">**GetMulticastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="bd193-179">**GetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="bd193-180">**GetUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="bd193-181">**InitializeUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="bd193-182">**IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="bd193-183">**IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="bd193-184">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="bd193-185">**SetUnicastIpAddressEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="bd193-186">Conversion de chaîne d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="bd193-186">IP address string conversion</span></span>

-   [<span data-ttu-id="bd193-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="bd193-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="bd193-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="bd193-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="bd193-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="bd193-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="bd193-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="bd193-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="bd193-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="bd193-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="bd193-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="bd193-195">Gestion des adresses IP voisines</span><span class="sxs-lookup"><span data-stu-id="bd193-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="bd193-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="bd193-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="bd193-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="bd193-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="bd193-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="bd193-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="bd193-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="bd193-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="bd193-202">**ResolveNeighbor**</span><span class="sxs-lookup"><span data-stu-id="bd193-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="bd193-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="bd193-204">Gestion des chemins d’accès IP</span><span class="sxs-lookup"><span data-stu-id="bd193-204">IP path management</span></span>

-   [<span data-ttu-id="bd193-205">**FlushIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="bd193-206">**GetIpPathEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="bd193-207">**GetIpPathTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="bd193-208">Gestion des itinéraires IP</span><span class="sxs-lookup"><span data-stu-id="bd193-208">IP route management</span></span>

-   [<span data-ttu-id="bd193-209">**CreateIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="bd193-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="bd193-211">**DeleteIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="bd193-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="bd193-213">**EnableRouter**</span><span class="sxs-lookup"><span data-stu-id="bd193-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="bd193-214">**GetBestInterface**</span><span class="sxs-lookup"><span data-stu-id="bd193-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="bd193-215">**GetBestInterfaceEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="bd193-216">**GetBestRoute**</span><span class="sxs-lookup"><span data-stu-id="bd193-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="bd193-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="bd193-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="bd193-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="bd193-219">**GetIpForwardTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="bd193-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="bd193-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="bd193-221">**GetRTTAndHopCount**</span><span class="sxs-lookup"><span data-stu-id="bd193-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="bd193-222">**InitializeIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="bd193-223">**SetIpForwardEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="bd193-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="bd193-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="bd193-225">**SetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="bd193-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="bd193-226">**SetIpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="bd193-227">**UnenableRouter**</span><span class="sxs-lookup"><span data-stu-id="bd193-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="bd193-228">Gestion de la mémoire de la table IP</span><span class="sxs-lookup"><span data-stu-id="bd193-228">IP table memory management</span></span>

-   [<span data-ttu-id="bd193-229">**FreeMibTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="bd193-230">Utilitaire IP</span><span class="sxs-lookup"><span data-stu-id="bd193-230">IP utility</span></span>

-   [<span data-ttu-id="bd193-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="bd193-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="bd193-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="bd193-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="bd193-233">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="bd193-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="bd193-234">**ParseNetworkString**</span><span class="sxs-lookup"><span data-stu-id="bd193-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="bd193-235">Configuration réseau</span><span class="sxs-lookup"><span data-stu-id="bd193-235">Network configuration</span></span>

-   [<span data-ttu-id="bd193-236">**GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="bd193-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="bd193-237">Notification</span><span class="sxs-lookup"><span data-stu-id="bd193-237">Notification</span></span>

-   [<span data-ttu-id="bd193-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="bd193-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="bd193-239">**NotifyAddrChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="bd193-240">**NotifyIpInterfaceChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="bd193-241">**NotifyRouteChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="bd193-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="bd193-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="bd193-243">**NotifyUnicastIpAddressChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="packet-timestamping"></a><span data-ttu-id="bd193-244">Horodatage des paquets</span><span class="sxs-lookup"><span data-stu-id="bd193-244">Packet timestamping</span></span>

-   [<span data-ttu-id="bd193-245">**CaptureInterfaceHardwareCrossTimestamp**</span><span class="sxs-lookup"><span data-stu-id="bd193-245">**CaptureInterfaceHardwareCrossTimestamp**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)
-   [<span data-ttu-id="bd193-246">**GetInterfaceActiveTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd193-246">**GetInterfaceActiveTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities)
-   [<span data-ttu-id="bd193-247">**GetInterfaceSupportedTimestampCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd193-247">**GetInterfaceSupportedTimestampCapabilities**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)
-   [<span data-ttu-id="bd193-248">**RegisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-248">**RegisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange)
-   [<span data-ttu-id="bd193-249">**UnregisterInterfaceTimestampConfigChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-249">**UnregisterInterfaceTimestampConfigChange**</span></span>](/windows/win32/api/iphlpapi/unregisterinterfacetimestampconfigchange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="bd193-250">Réservation de port persistant</span><span class="sxs-lookup"><span data-stu-id="bd193-250">Persistent port reservation</span></span>

-   [<span data-ttu-id="bd193-251">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-251">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="bd193-252">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-252">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="bd193-253">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-253">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="bd193-254">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-254">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="bd193-255">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-255">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="bd193-256">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bd193-256">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="bd193-257">Intégrité de la sécurité</span><span class="sxs-lookup"><span data-stu-id="bd193-257">Security health</span></span>

-   <span data-ttu-id="bd193-258">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd193-258">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="bd193-259">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd193-259">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="bd193-260">Ces fonctions sont définies uniquement sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bd193-260">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="bd193-261">Ces fonctions ne sont pas disponibles sur Windows Vista, ni sur Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bd193-261">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="bd193-262">Gestion du client IPv6 Teredo</span><span class="sxs-lookup"><span data-stu-id="bd193-262">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="bd193-263">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="bd193-263">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="bd193-264">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="bd193-264">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="bd193-265">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-265">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="bd193-266">Protocole TCP (Transmission Control Protocol) et UDP (User Datagram Protocol)</span><span class="sxs-lookup"><span data-stu-id="bd193-266">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="bd193-267">**GetExtendedTcpTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-267">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="bd193-268">**GetExtendedUdpTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-268">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="bd193-269">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="bd193-269">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="bd193-270">**GetOwnerModuleFromTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-270">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="bd193-271">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="bd193-271">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="bd193-272">**GetOwnerModuleFromUdpEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-272">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="bd193-273">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="bd193-273">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="bd193-274">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="bd193-274">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="bd193-275">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="bd193-275">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="bd193-276">**GetTcpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-276">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="bd193-277">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="bd193-277">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="bd193-278">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="bd193-278">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="bd193-279">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="bd193-279">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="bd193-280">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-280">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="bd193-281">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="bd193-281">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="bd193-282">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="bd193-282">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="bd193-283">**SetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="bd193-283">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="bd193-284">**SetTcpEntry**</span><span class="sxs-lookup"><span data-stu-id="bd193-284">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="bd193-285">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="bd193-285">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="bd193-286">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="bd193-286">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="bd193-287">**GetUdpStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="bd193-287">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="bd193-288">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="bd193-288">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="bd193-289">**GetUdpTable**</span><span class="sxs-lookup"><span data-stu-id="bd193-289">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="bd193-290">API déconseillées</span><span class="sxs-lookup"><span data-stu-id="bd193-290">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="bd193-291">Ces fonctions sont dépréciées et ne sont pas prises en charge par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd193-291">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="bd193-292">**AllocateAndGetTcpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="bd193-292">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="bd193-293">**AllocateAndGetUdpExTableFromStack**</span><span class="sxs-lookup"><span data-stu-id="bd193-293">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
