---
description: Les tableaux suivants décrivent les \_ options de socket IP IPPROTO qui s’appliquent aux sockets créés pour la famille d’adresses IPv4 (AF \_ inet). Consultez les pages de référence des fonctions getsockopt et setsockopt pour plus d’informations sur l’obtention et la définition des options de Socket.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: IPPROTO_IP socket, options
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530461"
---
# <a name="ipproto_ip-socket-options"></a>\_Options de socket IP IPPROTO

Les tableaux suivants décrivent **IPPROTO_IP** options de socket qui s’appliquent aux sockets créés pour la famille d’adresses IPv4 (AF \_ inet). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Certaines options de socket requièrent plus d’explications que celles pouvant être transmises par ces tables. ces options contiennent des liens vers des pages supplémentaires.

## <a name="options"></a>Options

| Option | Obtenir | Définissez | Type Optval | Description |
|-|-|-|-|-|
| IP_ADD_IFLIST | | Oui | DWORD (IF_INDEX) | Ajoute un index d’interface au IFLIST associé à l’option **IP_IFLIST** . |
| IP_ADD_MEMBERSHIP | | Oui | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Joindre le socket au groupe de multidiffusion fourni sur l’interface spécifiée. |
| IP_ADD_SOURCE_MEMBERSHIP | | Oui | [**\_source mreq \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Joindre le groupe de multidiffusion fourni sur l’interface donnée et accepter les données source à partir de l’adresse source fournie. |
| \_source de bloc IP \_ | | Oui | [**\_source mreq \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Supprime la source donnée en tant qu’expéditeur du groupe et de l’interface de multidiffusion fournis. |
| IP_DEL_IFLIST | | Oui | DWORD (IF_INDEX) | Supprime un index d’interface du IFLIST associé à l’option **IP_IFLIST** . Les entrées ne peuvent être supprimées que par l’application. sachez que les entrées peuvent être obsolètes une fois qu’une interface est supprimée. |
| \_DONTFRAGMENT IP | Oui | Oui | DWORD (booléen) | Indique que les données ne doivent pas être fragmentées, quelle que soit la MTU locale. Valide uniquement pour les protocoles orientés message. Les fournisseurs Microsoft TCP/IP respectent cette option pour UDP et ICMP. |
| \_appartenance IP Drop \_ | | Oui | [**\_mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Laisse le groupe de multidiffusion spécifié à partir de l’interface spécifiée. Les fournisseurs de services doivent prendre en charge cette option lorsque la multidiffusion est prise en charge. La prise en charge est indiquée dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retournée par un appel de fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) avec le code suivant : XPI \_ support \_ multipoint = 1, XP1 \_ multipoint \_ Control \_ plan = 0, XP1 \_ multipoint \_ Data \_ plan = 0. |
| appartenance à la \_ source de suppression IP \_ \_ | | Oui | [**\_source mreq \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Supprime l’appartenance au groupe de multidiffusion, à l’interface et à l’adresse source donnés. |
| IP_GET_IFLIST | Oui | | DWORD [] (IF_INDEX []) | Obtient le IFLIST actuel associé à l’option **IP_IFLIST** . Retourne une erreur si **IP_IFLIST** n’est pas activé. |
| \_HDRINCL IP | Oui | Oui | DWORD (booléen) | Quand la valeur est **true**, indique que l’application fournit l’en-tête IP. S’applique uniquement aux \_ sockets bruts de la chaussette. Le fournisseur de services TCP/IP peut définir le champ ID, si la valeur fournie par l’application est égale à zéro.  L' \_ option IP HDRINCL est appliquée uniquement au \_ type de protocole de la valeur brute de la chaussette. Un fournisseur de services TCP/IP qui prend en charge le brut de chaussette \_ doit également prendre en charge IP \_ HDRINCL.  |
| IP_IFLIST | Oui | Oui | DWORD (booléen) | Obtient ou définit l’état **IP_IFLIST** du Socket. Lorsque cette option a la valeur true, la réception du datagramme est limitée aux interfaces qui se trouvent dans le IFLIST. Les Datagrammes reçus sur toute autre interface sont ignorés. IFLIST démarre vide. Utilisez **IP_ADD_IFLIST** et **IP_DEL_IFLIST** pour modifier IFLIST. |
| \_MTU IP | Oui | | DWORD | Obtient l’estimation du système du chemin MTU. Le socket doit être connecté. |
| \_découverte MTU \_ IP | Oui | Oui | DWORD (**\_ État PMTUD**) | Obtient ou définit l’état de découverte MTU du chemin d’accès pour le Socket. La valeur par défaut est **IP \_ PMTUDISC \_ not \_ Set**. Pour les sockets de flux, les **\_ PMTUDISC IP ne sont \_ pas \_ définis** et les **\_ PMTUDISC IP \_** effectuent la détection de chemin MTU. **Adresse IP \_ PMTUDISC \_** et la **\_ \_ sonde IP PMTUDISC** désactivent la détection du chemin MTU. Pour les sockets de datagramme, les **\_ \_ PMTUDISC IP** forcent tous les paquets sortants à avoir le bit DF défini et une tentative d’envoi de paquets supérieur à Path MTU génère une erreur. **Adresse IP \_ PMTUDISC \_** ne force pas tous les paquets sortants à avoir un bit DF non défini, et les paquets sont fragmentés en fonction de l’interface MTU. **Adresse IP \_ La \_ sonde PMTUDISC** force tous les paquets sortants à avoir le bit DF défini et une tentative d’envoi de paquets supérieur à l’interface MTU génère une erreur. |
| multidiffusion IP \_ \_ si | Oui | Oui | DWORD | Obtient ou définit l’interface sortante pour l’envoi du trafic de multidiffusion IPv4. Cette option ne modifie pas l’interface par défaut pour la réception du trafic de multidiffusion IPv4.  La valeur d’entrée pour la définition de cette option est une adresse IPv4 de 4 octets dans l’ordre des octets du réseau. Ce paramètre DWORD peut également être un index d’interface dans l’ordre des octets du réseau. Toute adresse IP du bloc 0. x. x. x (premier octet de 0), à l’exception de l’adresse IPv4 0.0.0.0, est traitée comme un index d’interface. Un index d’interface est un nombre 24 bits et le bloc d’adresses IPv4 0.0.0.0/8 n’est pas utilisé (cette plage est réservée). L’index d’interface peut être utilisé pour spécifier l’interface par défaut pour le trafic de multidiffusion pour IPv4. Si *optval* est égal à zéro, l’interface par défaut pour la réception de la multidiffusion est spécifiée pour l’envoi du trafic de multidiffusion.  Lors de l’obtention de cette option, *optval* retourne l’index d’interface par défaut actuel pour l’envoi du trafic de multidiffusion IPv4 dans l’ordre d’octet de l’hôte. |
| \_boucle de multidiffusion IP \_ | Oui | Oui | DWORD (booléen) | Contrôle si les données envoyées par une application sur l’ordinateur local (pas nécessairement par le même socket) dans une session de multidiffusion sont reçues par un socket joint au groupe de destination de multidiffusion sur l’interface de bouclage. La valeur **true** entraîne la remise des données de multidiffusion envoyées par une application sur l’ordinateur local à un socket d’écoute sur l’interface de bouclage. La valeur **false** empêche la remise des données de multidiffusion envoyées par une application sur l’ordinateur local à un socket d’écoute sur l’interface de bouclage. Par défaut, **le \_ \_ Bouclage de multidiffusion IP** est activé. |
| \_TTL de multidiffusion IP \_ | Oui | Oui | DWORD | Définit/obtient la valeur de durée de vie associée au trafic de multidiffusion IP sur le Socket. |
| \_Options IP | Oui | Oui | Char \[\] | Spécifie les options IP à insérer dans les paquets sortants. La définition de nouvelles options remplace toutes les options spécifiées précédemment. La définition de optval sur zéro supprime toutes les options spécifiées précédemment. La \_ prise en charge des options IP n’est pas nécessaire ; pour vérifier si les \_ Options IP sont prises en charge, utilisez [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pour accéder aux options actuelles. Si **getsockopt** échoue, les \_ Options IP ne sont pas prises en charge. |
| \_arrivée d’origine d’IP \_ \_ si | Oui | Oui | DWORD (booléen) | Indique si la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) doit retourner des données de contrôle facultatives contenant l’interface d’arrivée dans laquelle le paquet a été reçu pour les sockets de datagrammes. Cette option permet à l’interface IPv4 où le paquet a été reçu d’être renvoyée dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Cette option est valide uniquement sur le datagramme et les sockets bruts (le type de socket doit être un \_ DGRAM chaussette ou un brut de chaussette \_ ). |
| [\_PKTINFO IP](ip-pktinfo.md) | Oui | Oui | DWORD | Indique que les informations de paquet doivent être retournées par la fonction **WSARecvMsg** . |
| \_diffusion de réception IP \_ | Oui | Oui | DWORD (booléen) | Autorise ou bloque la réception de diffusion. |
| \_RECVIF IP | Oui | Oui | DWORD (booléen) | Indique si la pile IP doit remplir la mémoire tampon de contrôle avec des détails sur l’interface qui a reçu un paquet avec un socket datagramme. Lorsque cette valeur est true, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant l’interface dans laquelle le paquet a été reçu pour les sockets de datagrammes. Cette option permet à l’interface IPv4 où le paquet a été reçu d’être renvoyée dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Cette option est valide uniquement sur le datagramme et les sockets bruts (le type de socket doit être un \_ DGRAM chaussette ou un brut de chaussette \_ ). |
| \_RECVTOS IP | Oui | Oui | DWORD (booléen) | Indique si la pile IP doit remplir la mémoire tampon de contrôle avec un message contenant le champ d’en-tête IPv4 du type de service (TOS) sur un datagramme reçu. Lorsque cette valeur est true, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des données de contrôle facultatives contenant la valeur du champ d’en-tête IPv4 TOS du datagramme reçu.  Cette option permet de retourner le champ d’en-tête IPv4 TOS du datagramme reçu dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . Le type de message retourné sera l’adresse IP \_ OT. Tous les bits DSCP et ECN du champ OT sont retournés.  Cette option est valide uniquement sur les sockets de datagrammes (le type de socket doit être un \_ DGRAM chaussette).  |
| \_RECVTTL IP | Oui | Oui | DWORD (booléen) | Indique que les informations de tronçon (TTL) doivent être retournées dans la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Si *optval* a la valeur **1** lors de l’appel à [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l’option est activée. Si la valeur est **0**, l’option est désactivée.  Cette option est valide uniquement pour le datagramme et les sockets bruts (le type de socket doit être une chaussette \_ DGRAM ou une semelle \_ brute). |
| \_TOS IP | Oui | Oui | DWORD (booléen) | Ne pas utiliser. Les paramètres de type de service (TOS) doivent uniquement être définis à l’aide de l’API Quality of service. Pour plus d’informations, consultez [services différenciés](/previous-versions/windows/desktop/qos/differentiated-services) dans la section qualité de service du kit de développement logiciel (SDK) de plateforme. |
| \_TTL IP | Oui | Oui | DWORD (booléen) | Modifie la valeur par défaut définie par le fournisseur de services TCP/IP dans le champ TTL de l’en-tête IP des datagrammes sortants. La \_ prise en charge de la durée de vie IP n’est pas requise ; pour vérifier si la \_ durée de vie IP est prise en charge, utilisez [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pour accéder aux options actuelles. Si **getsockopt** échoue, la \_ durée de vie IP n’est pas prise en charge. |
| \_source de déblocage IP \_ | | Oui | [**\_source mreq \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Ajoute la source donnée en tant qu’expéditeur au groupe et à l’interface de multidiffusion fournis. |
| monodiffusion IP \_ \_ si | Oui | Oui | DWORD (si \_ index) | Obtient ou définit l’interface sortante pour l’envoi du trafic IPv4. Cette option ne modifie pas l’interface par défaut pour la réception du trafic IPv4. Cette option est importante pour les ordinateurs multirésidents.  La valeur d’entrée pour la définition de cette option est une adresse IPv4 de 4 octets dans l’ordre des octets du réseau. Ce paramètre DWORD doit être un index d’interface dans l’ordre des octets du réseau. Toute adresse IP du bloc 0. x. x. x (premier octet de 0), à l’exception de l’adresse IPv4 0.0.0.0, est traitée comme un index d’interface. Un index d’interface est un nombre 24 bits et le bloc d’adresses IPv4 0.0.0.0/8 n’est pas utilisé (cette plage est réservée). L’index d’interface peut être utilisé pour spécifier l’interface par défaut pour l’envoi du trafic pour IPv4. La fonction [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) peut être utilisée pour obtenir les informations d’index de l’interface. Si *optval* est égal à zéro, l’interface par défaut pour l’envoi du trafic est définie sur non spécifié.  Lors de l’obtention de cette option, *optval* retourne l’index d’interface par défaut actuel pour l’envoi du trafic IPv4 dans l’ordre d’octet de l’hôte. |
| IP_USER_MTU | Oui | Oui | DWORD | Obtient ou définit une limite supérieure sur la MTU de la couche IP (en octets) pour le socket donné. Si la valeur est supérieure à l’estimation de l’unité de transmission maximale (MTU) du système (que vous pouvez récupérer sur un socket connecté en interrogeant l’option **IP_MTU** Socket), l’option n’a aucun effet. Si la valeur est inférieure, les paquets sortants supérieurs à ce nombre seront fragmentés ou ne pourront pas être envoyés, en fonction de la valeur de **IP_DONTFRAGMENT**. La valeur par défaut est **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Pour la sécurité de type, vous devez utiliser les fonctions [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) et [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) au lieu d’utiliser directement l’option de Socket. |
| \_contexte de \_ redirection \_ WFP IP | Oui | Oui | WSACMSGHDR avec données de contrôle | Un type de données connexe de socket datagramme ( \_ type CMSG) pour indiquer le contexte de redirection pour un socket UDP utilisé par un service de redirection de la plateforme de filtrage Windows (WFP) en mode utilisateur. |
| \_enregistrements de \_ redirection \_ WFP IP | Oui | Oui | WSACMSGHDR avec données de contrôle | Un type de données connexe de socket datagramme ( \_ type CMSG) pour indiquer l’enregistrement de redirection pour un socket UDP utilisé par un service de redirection de la plateforme de filtrage Windows (WFP) en mode utilisateur. |

## <a name="windows-support-for-ip_proto-options"></a>Prise en charge de Windows pour les \_ Options IP proto

| Option | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_Ajout d' \_ un abonnement IP | x | x | x | x | x | x |
| appartenance à une source d’ajout d’adresses IP \_ \_ \_ | x | x | x | x | x | x |
| \_source de bloc IP \_ | x | x | x | x | x | x |
| IP_DEL_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_DONTFRAGMENT IP | x | x | x | x | x | x |
| \_appartenance IP Drop \_ | x | x | x | x | x | x |
| appartenance à la \_ source de suppression IP \_ \_ | x | x | x | x | x | x |
| IP_GET_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| \_HDRINCL IP | x | x | x | x | x | x |
| IP_IFLIST | À compter de Windows 10, version 1803 | | | | | |
| multidiffusion IP \_ \_ si | x | x | x | x | x | x |
| \_boucle de multidiffusion IP \_ | x | x | x | x | x | x |
| \_TTL de multidiffusion IP \_ | x | x | x | x | x | x |
| \_Options IP | x | x | x | x | x | x |
| \_arrivée d’origine d’IP \_ \_ si | x | x | x | x | | |
| \_PKTINFO IP | x | x | x | x | x | x |
| \_diffusion de réception IP \_ | x | x | x | x | x | x |
| \_RECVIF IP | À compter de Windows 10, version 1703 | x | x | x | x | x |
| \_RECVTTL IP | x | | | | | |
| \_TOS IP | x | x | x | | | |
| \_TTL IP | x | x | x | x | x | x |
| \_source de déblocage IP \_ | x | x | x | x | x | x |
| monodiffusion IP \_ \_ si | x | x | x | x | x | x |
| \_contexte de \_ redirection \_ WFP IP | x | x | x | | | |
| \_enregistrements de \_ redirection \_ WFP IP | x | x | x | | | |

<br/>

| Option | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| \_Ajout d' \_ un abonnement IP | x | x |
| appartenance à une source d’ajout d’adresses IP \_ \_ \_ | x | x |
| \_source de bloc IP \_ | x | x |
| IP_DEL_IFLIST | | |
| \_DONTFRAGMENT IP | x | x |
| \_appartenance IP Drop \_ | x | x |
| appartenance à la \_ source de suppression IP \_ \_ | x | x |
| IP_GET_IFLIST | | |
| \_HDRINCL IP | x | x |
| IP_IFLIST | | |
| multidiffusion IP \_ \_ si | x | x |
| \_boucle de multidiffusion IP \_ | x | x |
| \_TTL de multidiffusion IP \_ | x | x |
| \_Options IP | x | x |
| \_arrivée d’origine d’IP \_ \_ si | | |
| \_PKTINFO IP | x | x |
| \_diffusion de réception IP \_ | x | x |
| \_RECVIF IP | | |
| \_RECVTTL IP | | |
| \_TOS IP | | |
| \_TTL IP | x | x |
| \_source de déblocage IP \_ | x | x |
| monodiffusion IP \_ \_ si | | |
| \_contexte de \_ redirection \_ WFP IP | | |
| \_enregistrements de \_ redirection \_ WFP IP | | |

## <a name="remarks"></a>Notes

Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et le niveau **\_ IP IPPROTO** est défini dans le fichier d’en-tête *Ws2def. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Certaines options de **socket \_ IP IPPROTO** sont définies dans le fichier d’en-tête *Ws2ipdef. h* , qui est inclus automatiquement par le fichier d’en-tête *Ws2tcpip. h* . Les autres options de socket **\_ IP IPPROTO** sont définies dans le fichier d’en-tête *Wsipv6ok. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Les fichiers d’en-tête *Ws2def. h*, *Ws2ipdef. h* et *Wsipv6ok. h* ne doivent jamais être utilisés directement.

Dans le kit de développement logiciel (SDK) de plateforme commercialisé pour Windows Server 2003 et Windows XP, le niveau d' **\_ adresse IP IPPROTO** est défini dans le fichier d’en-tête *Winsock2. h* . Certaines options de **socket \_ IP IPPROTO** sont définies dans le fichier d’en-tête *Ws2tcpip. h* . Les autres options de socket **\_ IP IPPROTO** sont définies dans le fichier d’en-tête *Wsipv6ok. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Le fichier d’en-tête *Wsipv6ok. h* ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | <dl> <dt>Ws2def. h (inclure Winsock2. h); </dt> <dt>Ws2ipdef. h (include Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (inclure Winsock2. h)</dt> </dl> |
