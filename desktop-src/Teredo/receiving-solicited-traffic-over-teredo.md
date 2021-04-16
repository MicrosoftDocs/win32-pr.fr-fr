---
title: Réception du trafic sollicité sur Teredo
description: De nombreuses applications, telles que Microsoft Internet Explorer et Microsoft Outlook, initient uniquement des connexions à Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104508174"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Réception du trafic sollicité sur Teredo

De nombreuses applications, telles que Microsoft Internet Explorer et Microsoft Outlook, initient uniquement des connexions à Internet. Pour ces applications, [Teredo](about-teredo.md) peut fournir une connectivité transparente sur IPv6 en l’absence d’autres interfaces IPv6. En outre, le trafic sollicité peut être reçu via l’interface Teredo sur les plateformes Microsoft Windows XP avec Service Pack 2 (SP2) et Windows Server 2003 antérieures.

La documentation suivante explique comment ces applications assurent la connectivité et les circonstances dans lesquelles Teredo est utilisé.

## <a name="obtaining-a-destination-address"></a>Obtention d’une adresse de destination

Une application tente d’obtenir l’adresse de destination à l’aide de différentes méthodes, telles que le DNS (Domain Name System) ou le protocole PNRP (Peer Name Resolution Protocol). L’application peut obtenir plusieurs adresses IP IPv4 et IPv6 à l’aide de ces méthodes. Les API standard utilisées pour obtenir les adresses IP incluent l’API Windows XP [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) et la nouvelle API Windows Vista [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Par exemple, l’utilisation de l’API GetAddrInfo avec le paramètre de la *\_ famille ai* définie sur AF \_ inet6 comme indicateur de addrinfo/protocole permet à l’utilisateur d’interroger les serveurs DNS pour les adresses IPv6, en particulier. L’API [**DNSQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) avec le type DNS \_ \_ aaaa peut également être utilisée pour interroger les serveurs DNS pour les enregistrements aaaa.

## <a name="establishing-a-connection"></a>Établissement d’une connexion

Une connexion établie avec Teredo est décrite comme « transparente », car elle est gérée comme toute autre connexion IPv6. La programmation d’une application ne nécessite pas une attention particulière pour pouvoir utiliser l’interface Teredo. Lorsqu’une connexion est établie entre des interfaces Teredo, il n’est pas nécessaire d’avoir un routeur de relais, typique de 6to4 et d’autres interfaces natives. Toutefois, Teredo est conçu comme une technologie de transition en dernier ressort pour la connectivité IPv6.

> [!Note]  
> Teredo n’est pas utilisé si le nom d’hôte fourni est résolu en adresses IPv4 uniquement.

 

Quand une application tente de se connecter à une destination à l’aide d’adresses IPv6, voici ce qui se produit :

-   L’application obtient une liste d’adresses IPv6 en appelant l’API [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) . La pile Windows Vista retourne une liste de toutes les interfaces en fonction de l’ordre de tri spécifié dans le [document RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Par conséquent, les interfaces IPv6 et 6to4 IPv6 seront listées avant l’interface Teredo. Toutefois, lorsque la connectivité IPv6 native ou 6to4 n’est pas disponible, Teredo est la seule interface compatible IPv6 listée.

    Il est important de se souvenir qu’une application peut utiliser n’importe quelle interface fournie par la pile Windows Vista, mais le classement de la liste d’interfaces retournée entraînera généralement la tentative de la dernière tentative de Teredo.

-   Avant que Windows Vista tente une connexion sur l’interface Teredo, le système d’exploitation s’assure que l’adresse IPv6 est stabilisée. Cela s’effectue automatiquement pour les connexions sortantes et n’est pas un facteur crucial pour une application. Dans le cas où l’application est requise pour garantir la stabilité des adresses, l’API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) peut être appelée pour s’assurer que l’adresse Teredo est stable.

-   Une interface Teredo tentera de se connecter à une autre interface Teredo à la destination. Si aucune interface Teredo n’est présente, une connexion est établie avec une adresse de destination native ou 6to4 via un relais spécifique à l’hôte.

Il est également possible pour les applications qui initient des connexions à Internet de recevoir du trafic non sollicité. Pour plus d’informations, consultez [réception de trafic non sollicité sur Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Utilisation de l’API WSAConnectByName

En appelant l’API WSAConnectByName, il est possible pour une application de se connecter à un nom de destination au lieu de spécifier l’adresse IP exacte. La pile Windows Vista préfère IPv6 sur IPv4 et, par conséquent, toutes les tentatives de connexion seront d’abord effectuées sur les adresses IPv6.

L’appel de l’API WSAConnectByName trie toutes les adresses IP de destination obtenues dans l’ordre suivant :

-   Adresse IPv6 native
-   adresse IP 6to4
-   Adresse IPv4
-   Adresse Teredo

Une fois les adresses de destination triées en interne, une connexion à la destination est tentée en fonction du meilleur itinéraire disponible sur l’hôte local pour l’adresse de destination. Comme indiqué par l’ordre des adresses triées, si le nom de destination correspond à une adresse IPv4 et Teredo, l’adresse IPv4 est utilisée pour établir la connexion.

L’API WSAConnectByName fonctionne en interne afin de trouver la meilleure correspondance entre les adresses. Cette tentative est basée sur les itinéraires disponibles sur l’hôte local et les adresses de destination.

En raison de l’absence actuelle de relais Teredo sur Internet, il est peu probable que les connexions aux adresses IPv6 natives aboutissent sur l’interface Teredo. Si WSAConnectByName est appelé, Windows Vista n’émet pas de requêtes AAAA quand Teredo est la seule interface compatible IPv6 disponible. Cela permet de s’assurer que les adresses IPv6 natives ne sont pas obtenues comme destination et que les connexions sont tentées sur IPv4, ce qui a le plus de chances de réussir. Pour obtenir des adresses IPv6 quand Teredo est la seule interface compatible IPv6, une application doit utiliser explicitement l’API DnsQuery pour les enregistrements AAAA.

 

 