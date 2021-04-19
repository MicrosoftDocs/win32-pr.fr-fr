---
description: Les tableaux suivants décrivent les \_ options de socket IPv6 IPPROTO qui s’appliquent aux sockets créés pour la famille d’adresses IPv6 (AF \_ inet6). Consultez les pages de référence des fonctions getsockopt et setsockopt pour plus d’informations sur l’obtention et la définition des options de Socket.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: IPPROTO_IPV6 socket, options
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 1ceaf08c2a59a24b9ff694ac9ff42b28fbf18480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542542"
---
# <a name="ipproto_ipv6-socket-options"></a>\_Options de socket IPv6 IPPROTO

Les tableaux suivants décrivent les options de socket **\_ IPv6 IPPROTO** qui s’appliquent aux sockets créés pour la famille d’adresses IPv6 (AF \_ inet6). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Certaines options de socket requièrent plus d’explications que celles pouvant être transmises par ces tables. ces options contiennent des liens vers des informations supplémentaires.

## <a name="options"></a>Options

| Option | get | set | Type Optval | Description |
|-|-|-|-|-|
| \_arrivée d’origine d’IP \_ \_ si | Oui | Oui | DWORD (booléen) | Indique si la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) doit retourner des données de contrôle facultatives contenant l’interface d’arrivée d’origine où le paquet a été reçu pour les sockets de datagrammes. Cette option est utilisée avec les protocoles de transition IPv6 (6to4, ISATAP et Teredo, par exemple) qui fournissent l’attribution d’adresses et le tunneling automatique hôte à hôte pour le trafic IPv6 monodiffusion lorsque les hôtes IPv6 doivent traverser des réseaux adresse IP4 pour atteindre d’autres réseaux IPv6. Les paquets IPv6 sont « tunnelés » sous la forme de paquets IPv4. Cette option permet à l’interface IPv4 d’origine où le paquet a été reçu d’être renvoyée dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  |
| IPV6_ADD_IFLIST | | Oui | DWORD (IF_INDEX) | Ajoute un index d’interface au IFLIST associé à l’option **IP_IFLIST** . |
| \_Ajouter une \_ appartenance IPv6 | | Oui | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Joindre le socket au groupe de multidiffusion fourni sur l’interface spécifiée.  Cette option est valide uniquement sur le datagramme et les sockets bruts (le type de socket doit être un \_ DGRAM chaussette ou un brut de chaussette \_ ). |
| IPV6_DEL_IFLIST | | Oui | DWORD (IF_INDEX) | Supprime un index d’interface du IFLIST associé à l’option **IP_IFLIST** . Les entrées ne peuvent être supprimées que par l’application. sachez que les entrées peuvent être obsolètes une fois qu’une interface est supprimée. |
| \_Adhésion à Drop IPv6 \_ | | Oui | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Laisse le groupe de multidiffusion fourni à partir de l’interface donnée.  Cette option est valide uniquement sur le datagramme et les sockets bruts (le type de socket doit être un \_ DGRAM chaussette ou un brut de chaussette \_ ). |
| IPV6_GET_IFLIST | Oui | | DWORD [] (IF_INDEX []) | Obtient le IFLIST actuel associé à l’option **IP_IFLIST** . Retourne une erreur si **IP_IFLIST** n’est pas activé. |
| \_HDRINCL IPv6 | Oui | Oui | DWORD (booléen) | Indique que l’application fournit l’en-tête IPv6 sur toutes les données sortantes. Si le paramètre *optval* a la valeur **1** lors de l’appel à [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l’option est activée. Si *optval* a la valeur **0**, l’option est désactivée. La valeur par défaut est Désactivé. Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). Un fournisseur de services TCP/IP qui prend en charge le brut de chaussette \_ doit également prendre en charge les \_ HDRINCL IPv6. |
| \_HOPLIMIT IPv6 | Oui | Oui | DWORD (booléen) | Indique que les informations de tronçon (TTL) doivent être retournées dans la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Si *optval* a la valeur **1** lors de l’appel à [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l’option est activée. Si la valeur est **0**, l’option est désactivée.  Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). |
| IPV6_IFLIST | Oui | Oui | DWORD (booléen) | Obtient ou définit l’état **IP_IFLIST** du Socket. Lorsque cette option a la valeur true, la réception du datagramme est limitée aux interfaces qui se trouvent dans le IFLIST. Les Datagrammes reçus sur toute autre interface sont ignorés. IFLIST démarre vide. Utilisez **IP_ADD_IFLIST** et **IP_DEL_IFLIST** pour modifier IFLIST. |
| \_Groupe de jointure IPv6 \_ | | Oui | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identique à IPV6 \_ Ajouter une \_ appartenance |
| IPV6- \_ conserver le \_ groupe | | Oui | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Identique à \_ \_ l’adhésion à la suppression IPv6 |
| \_MTU IPv6 | Oui | | DWORD | Obtient l’estimation du système du chemin MTU. Le socket doit être connecté. |
| \_Détection IPv6 MTU \_ | Oui | Oui | DWORD (**\_ État PMTUD**) | Obtient ou définit l’état de découverte MTU du chemin d’accès pour le Socket. La valeur par défaut est **IP \_ PMTUDISC \_ not \_ Set**. Pour les sockets de flux, les **\_ PMTUDISC IP ne sont \_ pas \_ définis** et les **\_ PMTUDISC IP \_** effectuent la détection de chemin MTU. **Adresse IP \_ PMTUDISC \_** et la **\_ \_ sonde IP PMTUDISC** désactivent la détection du chemin MTU. Pour les sockets de datagrammes, si la valeur **IP \_ PMTUDISC \_ do** , les tentatives d’envoi de paquets supérieurs à Path MTU génèrent une erreur. Si la valeur **IP \_ PMTUDISC \_** n’est pas définie, les paquets sont fragmentés en fonction de l’interface MTU. Si la valeur est définie sur la **\_ \_ sonde IP PMTUDISC**, les tentatives d’envoi de paquets supérieurs à l’interface MTU provoquent une erreur.  |
| \_Tronçons de multidiffusion IPv6 \_ | Oui | Oui | DWORD | Obtient ou définit la valeur de durée de vie associée au trafic de multidiffusion IPv6 sur le Socket. Il est interdit de définir la durée de vie sur une valeur supérieure à 255.  Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). |
| Multidiffusion IPV6 \_ \_ si | Oui | Oui | DWORD | Obtient ou définit l’interface sortante pour l’envoi du trafic de multidiffusion IPv6. Cette option ne modifie pas l’interface par défaut pour la réception du trafic de multidiffusion IPv6. Cette option est importante pour les ordinateurs multirésidents.  La valeur d’entrée pour la définition de cette option est un index d’interface de 4 octets de l’interface sortante souhaitée dans l’ordre d’octet de l’hôte. La fonction [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) peut être utilisée pour obtenir les informations d’index de l’interface. Si *optval* a la valeur **null** lors de l’appel à [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l’interface IPv6 par défaut est utilisée. Si *optval* est égal à zéro, l’interface par défaut pour la réception de la multidiffusion est spécifiée pour l’envoi du trafic de multidiffusion.  Lors de l’obtention de cette option, *optval* retourne l’index d’interface par défaut actuel pour l’envoi du trafic IPv6 de multidiffusion dans l’ordre d’octet de l’hôte. |
| \_Boucle de multidiffusion IPv6 \_ | Oui | Oui | DWORD (booléen) | Indique que les données de multidiffusion envoyées sur le socket sont répercutées dans la mémoire tampon de réception des sockets si elles sont également jointes au groupe de multidiffusion de destination. Si *optval* a la valeur **1** lors de l’appel à [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l’option est activée. Si la valeur est **0**, l’option est désactivée.  Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). |
| [\_PKTINFO IPv6](ipv6-pktinfo.md) | Oui | Oui | DWORD (booléen) | Indique que les informations de paquet doivent être retournées par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . |
| [\_Niveau de protection IPv6 \_](ipv6-protection-level.md) | Oui | Oui | INT | Active la restriction d’un socket à une portée spécifiée, telle que les adresses avec le même préfixe de lien local ou de site local. Fournit différents niveaux de restriction et paramètres par défaut. Pour plus d’informations, consultez [ \_ \_ niveau de protection IPv6](ipv6-protection-level.md) . |
| \_RECVIF IPv6 | Oui | Oui | DWORD (booléen) | Indique si la pile IP doit remplir la mémoire tampon de contrôle avec des détails sur l’interface qui a reçu un paquet avec un socket datagramme. Lorsque cette valeur est true, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant l’interface dans laquelle le paquet a été reçu pour les sockets de datagrammes. Cette option permet à l’interface IPv6 dans laquelle le paquet a été reçu d’être renvoyée dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). |
| \_RECVTCLASS IPv6 | Oui | Oui | DWORD (booléen) | Indique si la pile IP doit remplir la mémoire tampon de contrôle avec un message contenant le champ d’en-tête IPv6 de classe de trafic sur un datagramme reçu. Lorsque cette valeur est true, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant la valeur du champ d’en-tête IPv6 de la classe de trafic du datagramme reçu.  Cette option permet de renvoyer le champ d’en-tête IPv6 de classe de trafic du datagramme reçu dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . Le type de message retourné sera IPV6 \_ TCLASS. Tous les bits DSCP et ECN du champ de classe de trafic sont retournés.  Cette option est valide uniquement sur les sockets de datagrammes (le type de socket doit être un \_ DGRAM chaussette).  |
| \_Tronçons de monodiffusion IPv6 \_ | Oui | Oui | DWORD | Obtient ou définit la valeur de durée de vie actuelle associée au socket IPv6 pour le trafic monodiffusion. Il est interdit de définir la durée de vie sur une valeur supérieure à 255. |
| Monodiffusion IPV6 \_ \_ si | Oui | Oui | DWORD (si \_ index) | Obtient ou définit l’interface sortante pour l’envoi du trafic IPv6. Cette option ne modifie pas l’interface par défaut pour la réception du trafic IPv6. Cette option est importante pour les ordinateurs multirésidents.  La valeur d’entrée pour la définition de cette option est un index d’interface de 4 octets de l’interface sortante souhaitée dans l’ordre d’octet de l’hôte. La fonction [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) peut être utilisée pour obtenir les informations d’index de l’interface. Si *optval* est égal à zéro, l’interface par défaut pour l’envoi du trafic IPv6 est définie sur non spécifié.  Lors de l’obtention de cette option, *optval* retourne l’index d’interface par défaut actuel pour l’envoi du trafic IPv6 dans l’ordre d’octet de l’hôte. |
| IPV6_USER_MTU | Oui | Oui | DWORD | Obtient ou définit une limite supérieure sur la MTU de la couche IP (en octets) pour le socket donné. Si la valeur est supérieure à l’estimation de l’unité de transmission maximale (MTU) du système (que vous pouvez récupérer sur un socket connecté en interrogeant l’option **IPV6_MTU** Socket), l’option n’a aucun effet. Si la valeur est inférieure, les paquets sortants supérieurs à ce nombre seront fragmentés ou ne pourront pas être envoyés, en fonction de la valeur de **IPV6_DONTFRAG**. La valeur par défaut est **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Pour la sécurité de type, vous devez utiliser les fonctions [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) et [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) au lieu d’utiliser directement l’option de Socket. |
| \_V6ONLY IPv6 | Oui | Oui | DWORD (booléen) | Indique si un socket créé pour la famille d’adresses inet6 de la catégorie \_ inet6 est limité uniquement aux communications IPv6. Les sockets créés pour la famille d’adresses inet6 de la même façon \_ peuvent être utilisés pour les communications IPv6 et IPv4. Certaines applications peuvent souhaiter limiter leur utilisation d’un socket créé pour les communications de la famille d’adresses de l' \_ adresse inet6 à IPv6 uniquement. Lorsque cette valeur est différente de zéro (valeur par défaut sur Windows), un socket créé pour la \_ famille d’adresses inet6 de la même façon peut être utilisé pour envoyer et recevoir des paquets IPv6 uniquement. Lorsque cette valeur est égale à zéro, un socket créé pour la \_ famille d’adresses inet6 inet6 peut être utilisé pour envoyer et recevoir des paquets vers et depuis une adresse IPv6 ou une adresse IPv4. Notez que pour interagir avec une adresse IPv4, l'utilisation d'adresses IPv4 mappées est requise. Cette option de socket est prise en charge sous Windows Vista ou versions ultérieures. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Prise en charge de Windows pour les \_ options de socket IPv6 IPPROTO

| Option | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| \_arrivée d’origine d’IP \_ \_ si | x | x | x | | |
| IPV6_ADD_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_Ajouter une \_ appartenance IPv6 | x | x | x | x | x |
| IPV6_DEL_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_Adhésion à Drop IPv6 \_ | x | x | x | x | x |
| IPV6_GET_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_HDRINCL IPv6 | x | x | x | x | x |
| \_HOPLIMIT IPv6 | x | x | x | x | x |
| IPV6_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_Groupe de jointure IPv6 \_ | x | x | x | x | x |
| IPV6- \_ conserver le \_ groupe | x | x | x | x | x |
| \_Tronçons de multidiffusion IPv6 \_ | x | x | x | x | x |
| Multidiffusion IPV6 \_ \_ si | x | x | x | x | x |
| \_Boucle de multidiffusion IPv6 \_ | x | x | x | x | x |
| \_PKTINFO IPv6 | x | x | x | x | x |
| [\_Niveau de protection IPv6 \_](ipv6-protection-level.md) | x | x | x | x | x |
| \_RECVIF IPv6 | x | x | x | x | x |
| \_Tronçons de monodiffusion IPv6 \_ | x | x | x | x | x |
| Monodiffusion IPV6 \_ \_ si | x | x | x | x | x |
| \_V6ONLY IPv6 | x | x | x | x | x |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| \_arrivée d’origine d’IP \_ \_ si | | |
| IPV6_ADD_IFLIST | | |
| \_Ajouter une \_ appartenance IPv6 | x | x |
| IPV6_DEL_IFLIST | | |
| \_Adhésion à Drop IPv6 \_ | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| \_Groupe de jointure IPv6 \_ | x | x |
| IPV6- \_ conserver le \_ groupe | x | x |
| \_Tronçons de multidiffusion IPv6 \_ | x | x |
| Multidiffusion IPV6 \_ \_ si | x | x |
| \_Boucle de multidiffusion IPv6 \_ | x | x |
| \_PKTINFO IPv6 | x | x |
| [\_Niveau de protection IPv6 \_](ipv6-protection-level.md) | x | x |
| \_RECVIF IPv6 | | |
| \_Tronçons de monodiffusion IPv6 \_ | x | x |
| Monodiffusion IPV6 \_ \_ si | | |
| \_V6ONLY IPv6 | | |

## <a name="remarks"></a>Notes

Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et le niveau **\_ IPv6 IPPROTO** est défini dans le fichier d’en-tête *Ws2def. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Les options de socket **\_ IPv6 IPPROTO** sont définies dans le fichier d’en-tête *Ws2ipdef. h* qui est automatiquement inclus dans le fichier d’en-tête *Ws2tcpip. h* . Les fichiers d’en-tête *Ws2def. h* et *Ws2ipdef. h* ne doivent jamais être utilisés directement.

L' \_ option d’arrivée d’origine IP \_ si le \_ Socket est pris en charge sur Windows Server 2008 R2 et sur Windows 7.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | <dl> <dt>Ws2def. h (inclure Winsock2. h); </dt> <dt>Winsock2. h sur Windows Server 2003 et Windows XP</dt> </dl> |
