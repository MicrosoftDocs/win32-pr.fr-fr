---
description: Nouveautés du programme d’assistance IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Nouveautés du programme d’assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c1a6eebb3e9e785e8988b822df0b2a80ae6eba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094525"
---
# <a name="whats-new-in-ip-helper"></a>Nouveautés du programme d’assistance IP

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 et Windows Server 2012

les fonctionnalités suivantes ont été ajoutées aux api d’assistance IP sur Windows 8 et Windows Server 2012.

Fonction qui récupère les estimations historiques de la bande passante pour une connexion réseau. Pour plus d'informations, consultez les pages suivantes :

-   [**GetIpNetworkConnectionBandwidthEstimates**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Structure qui contient des informations sur les estimations de bande passante disponibles et la variance associée comme déterminé par la pile TCP/IP. Pour plus d'informations, consultez les pages suivantes :

-   [**\_informations sur la bande passante NL \_**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

les fonctionnalités suivantes ont été ajoutées aux api d’assistance IP sur Windows 7 et Windows Server 2008 R2.

Fonctions qui convertissent une adresse Ethernet entre un format binaire et un format de chaîne pour l’adresse MAC Ethernet. Pour plus d'informations, consultez les pages suivantes :

-   [**RtlEthernetAddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**RtlEthernetStringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 et Windows Vista SP1

les fonctions suivantes ont été ajoutées aux api d’assistance IP sur Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

Fonction qui fonctionne avec IPv4 et le protocole ICMP (Internet Control Message Protocol). Pour plus d'informations, consultez les pages suivantes :

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

les groupes de fonctions suivants ont été ajoutés aux api d’assistance IP sur Windows Vista et versions ultérieures.

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la conversion de l’interface. Pour plus d'informations, consultez les pages suivantes :

-   [**ConvertInterfaceAliasToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**ConvertInterfaceGuidToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**ConvertInterfaceIndexToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**ConvertInterfaceLuidToGuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**ConvertInterfaceLuidToIndex**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**ConvertInterfaceLuidToNameA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**ConvertInterfaceLuidToNameW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**ConvertInterfaceNameToLuidA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**ConvertInterfaceNameToLuidW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**Si \_ indextoname**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**Si \_ nametoindex**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la gestion des interfaces. Pour plus d'informations, consultez les pages suivantes :

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**GetInvertedIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**GetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**GetIpInterfaceTable**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**InitializeIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**SetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la gestion des adresses IP. Pour plus d'informations, consultez les pages suivantes :

-   [**CreateAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**CreateUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**DeleteAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**DeleteUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**GetAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**GetAnycastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**GetMulticastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**GetMulticastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**GetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**GetUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**InitializeUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**SetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Fonction qui fonctionne avec les protocoles IPv6 et IPv4 pour la gestion de la mémoire de la table IP. Pour plus d'informations, consultez les pages suivantes :

-   [**FreeMibTable**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la gestion des adresses IP voisines. Pour plus d'informations, consultez les pages suivantes :

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ResolveNeighbor**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la gestion des chemins d’accès IP. Pour plus d'informations, consultez les pages suivantes :

-   [**FlushIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**GetIpPathEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**GetIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la gestion des itinéraires IP. Pour plus d'informations, consultez les pages suivantes :

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**InitializeIpForwardEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**SetIpStatisticsEx**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Fonctions qui fonctionnent avec les protocoles IPv6 et IPv4 pour la notification. Pour plus d'informations, consultez les pages suivantes :

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**NotifyIpInterfaceChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**NotifyUnicastIpAddressChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Fonctions utilitaires qui fonctionnent avec des adresses IP. Pour plus d'informations, consultez les pages suivantes :

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**CreateSortedAddressPairs**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**ParseNetworkString**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Fonctions qui fonctionnent avec le protocole TCP (Transmission Control Protocol) et UDP (User Datagram Protocol) pour récupérer la table de connexion TCP ou IPv4 IPv4 ou la table de l’écouteur UDP. Pour plus d'informations, consultez les pages suivantes :

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Fonctions qui fonctionnent avec le protocole TCP (Transmission Control Protocol) pour récupérer des statistiques TCP étendues sur une connexion. Pour plus d'informations, consultez les pages suivantes :

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**GetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**SetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Nouvelles fonctions qui fonctionnent pour la gestion du client IPv6 Teredo. Pour plus d'informations, consultez les pages suivantes :

-   [**GetTeredoPort**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Fonctions utilitaires qui fournissent des conversions entre des adresses IP et des représentations sous forme de chaîne d’adresses IP. Pour plus d'informations, consultez les pages suivantes :

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Fonctions qui fournissent des réservations persistantes pour un bloc consécutif de ports TCP ou UDP sur l’ordinateur local. Pour plus d'informations, consultez les pages suivantes :

-   [**CreatePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**CreatePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**DeletePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**DeletePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**LookupPersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**LookupPersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

les fonctions suivantes ont été ajoutées aux api d’assistance IP sur Windows Server 2003 et versions ultérieures :

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP SP2

les fonctions suivantes ont été ajoutées aux api d’assistance IP sur Windows XP avec Service Pack 2 (SP2) et versions ultérieures :

-   [**GetOwnerModuleFromTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**GetOwnerModuleFromUdpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
