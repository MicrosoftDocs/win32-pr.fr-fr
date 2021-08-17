---
description: Les tableaux suivants décrivent les \_ options de socket IPX NSPROTO qui s’appliquent aux sockets créés pour la famille d’adresses IPX/SPX (AF \_ IPX). Consultez les pages de référence des fonctions getsockopt et setsockopt pour plus d’informations sur l’obtention et la définition des options de Socket.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: Options de socket NSPROTO_IPX (Wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6803b5ab6cdf3002a60726c30648a1ae61bb59430820f049aeb8b011f367e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993629"
---
# <a name="nsproto_ipx-socket-options"></a>\_Options de socket IPX NSPROTO

Les tableaux suivants décrivent les options de socket **\_ IPX NSPROTO** qui s’appliquent aux sockets créés pour la famille d’adresses IPX/SPX (AF \_ IPX). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**\_Options de socket IPX NSPROTO**</dt> <dd> <dl> <dt> 

| Option                      | Obtenir | Définissez | Type Optval                  | Description                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_adresse IPX                | oui |     | **\_données d’adresse IPX \_**       | Retourne des informations sur l’adaptateur spécifique sur lequel IPX est activé.                                                                                                                                                                                                          |
| \_notification d’adresse IPX \_        | oui |     | **\_données d’adresse IPX \_**       | Notifie de manière asynchrone quand l’état d’un adaptateur IPX change.                                                                                                                                                                                                              |
| \_DSTYPE IPX                 | oui | oui | DWORD                        | Obtient ou définit la valeur du champ Datastream dans l’en-tête SPX à utiliser pour envoyer des paquets.                                                                                                                                                                                          |
| \_adresse IPX étendue \_      |     | oui | DWORD (booléen)              | Active l’option d’adressage étendu sur les paquets IPX.                                                                                                                                                                                                                          |
| \_FILTERPTYPE IPX            | oui | oui | DWORD                        | Obtient ou définit le type de paquet de filtre de réception IPX actuel. Seuls les paquets IPX avec un type de paquet égal à la valeur spécifiée dans le paramètre optval sont retournés. Les paquets avec un type de paquet qui ne correspond pas sont ignorés. Cela s’applique uniquement à un socket datagramme. |
| \_GETNETINFO IPX             | oui |     | **\_données IPX NETNUM \_**        | Retourne des informations concernant un numéro de réseau IPX spécifique. Le membre netnum de la structure de **\_ \_ données IPX netnum** doit être défini sur le numéro de réseau IPX à retourner.                                                                                                     |
| IPX \_ GETNETINFO \_ NORIP      | oui |     | **\_données IPX NETNUM \_**        | Retourne des informations concernant un numéro de réseau IPX spécifique sans envoyer de demande RIP. Le membre netnum de la structure de **\_ \_ données IPX netnum** doit être défini sur le numéro de réseau IPX à retourner.                                                                       |
| \_IMMEDIATESPXACK IPX        |     | oui | DWORD (booléen)              | Si la valeur est **true**, ne retardez pas l’envoi d’accusés de réception sur une connexion SPX.                                                                                                                                                                                                             |
| \_nombre maximal d' \_ ADAPTATEURs IPX \_      | oui |     | DWORD                        | Retourne le nombre d’adaptateurs compatibles IPX présents.                                                                                                                                                                                                                             |
| valeur IPX \_ MaxSize                | oui |     | DWORD                        | Retourne la taille maximale de datagramme IPX en octets qui peut être envoyée.                                                                                                                                                                                                                |
| \_PTYPE IPX                  | oui | oui | DWORD                        | Obtient ou définit le type de paquet. La valeur spécifiée dans le paramètre optval sera définie en tant que type de paquet sur chaque paquet IPX envoyé à partir de ce Socket.                                                                                                                             |
| \_diffusion de réception IPX \_     |     | oui | DWORD (booléen)              | Si la valeur est **true**, les paquets IPX de diffusion sont reçus.                                                                                                                                                                                                                              |
| \_RECVHDR IPX                |     | oui | DWORD (booléen)              | Si la valeur est **true**, les en-têtes de protocole IPX sont reçus avec des données.                                                                                                                                                                                                                     |
| \_RERIPNETNUMBER IPX         | oui |     | **\_données IPX NETNUM \_**        | Retourne des informations concernant un numéro de réseau IPX spécifié à l’aide d’une nouvelle requête RIP. Le membre netnum de la structure de **\_ \_ données IPX netnum** doit être défini sur le numéro de réseau IPX à retourner.                                                                            |
| \_SPXGETCONNECTIONSTATUS IPX | oui |     | **\_données IPX SPXCONNSTATUS \_** | Retourne des informations concernant les statistiques de socket SPX connectées.                                                                                                                                                                                                                |
| \_STOPFILTERPTYPE IPX        |     | oui | DWORD                        | Supprime le filtre et arrête le filtrage sur le type de paquet spécifié dans le paramètre optval.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Windows Prise en charge des \_ options IPX NSPROTO**</dt> <dd> <dl> <dt> 

| Option                      | Windows Vista et versions ultérieures | Windows Server 2003 | Windows XP | Windows 2000 | Windows 4 | Windows 9x/Me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_adresse IPX                |                         | x                   | x          | x            | x           | x             |
| \_notification d’adresse IPX \_        |                         | x                   | x          | x            | x           | x             |
| \_DSTYPE IPX                 |                         | x                   | x          | x            | x           | x             |
| \_adresse IPX étendue \_      |                         | x                   | x          | x            | x           | x             |
| \_FILTERPTYPE IPX            |                         | x                   | x          | x            | x           | x             |
| \_GETNETINFO IPX             |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO \_ NORIP      |                         | x                   | x          | x            | x           | x             |
| \_IMMEDIATESPXACK IPX        |                         | x                   | x          | x            | x           | x             |
| \_nombre maximal d' \_ ADAPTATEURs IPX \_      |                         | x                   | x          | x            | x           | x             |
| valeur IPX \_ MaxSize                |                         | x                   | x          | x            | x           | x             |
| \_PTYPE IPX                  |                         | x                   | x          | x            | x           | x             |
| \_diffusion de réception IPX \_     |                         | x                   | x          | x            | x           | x             |
| \_RECVHDR IPX                |                         | x                   | x          | x            | x           | x             |
| \_RERIPNETNUMBER IPX         |                         | x                   | x          | x            | x           | x             |
| \_SPXGETCONNECTIONSTATUS IPX |                         | x                   | x          | x            | x           | x             |
| \_STOPFILTERPTYPE IPX        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

les options de socket **\_ ipx NSPROTO** suivantes ont été définies dans Windows sockets 2 Protocol-Specific annexe, mais ne sont pas implémentées par le protocole IPX/SPX Windows.

de *niveau* **=** **NSPROTO \_ Protocole IPX**



| Option           | Type | Default                         | Signification                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_somme de contrôle IPX    | Bool | arrêt                             | Lorsqu’il est défini, le protocole IPX effectue une somme de contrôle sur les paquets sortants et vérifie la somme de contrôle des paquets entrants.                                                          |
| \_TXPKTSIZE IPX   | int  | Taille du média à un maximum de 1466 | Définit la taille maximale du datagramme d’envoi. Cette taille n’inclut pas l’en-tête IPX ou les en-têtes de support qui peuvent également être utilisés. Peut être augmentée à la taille du média.    |
| \_RXPKTSIZE IPX   | int  | Taille du média à un maximum de 1466 | Définit la taille maximale de datagramme de réception. Cette taille n’inclut pas l’en-tête IPX ou les en-têtes de support qui peuvent également être utilisés. Peut être augmentée à la taille du média. |
| \_TXMEDIASIZE IPX | int  | Tableau principal                   | Retourne la taille du média d’envoi qui définit une limite supérieure pour la taille du datagramme.                                                                                       |
| \_RXMEDIASIZE IPX | int  | Tableau principal                   | Retourne la taille du média de réception qui définit une limite supérieure pour la taille du datagramme.                                                                                    |
| réplica \_ principal IPX     | Bool | Principal                         | Limite le trafic à la carte réseau principale.                                                                                                               |



 

les options de socket **NSPROTO \_ SPX** suivantes ont été définies dans Windows sockets 2 Protocol-Specific annexe, mais ne sont pas implémentées sur Windows par le protocole Windows IPX/SPX.

de *niveau* **=** **NSPROTO \_ SPX**



| Option           | Type | Default                         | Signification                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_somme de contrôle SPX    | Bool | arrêt                             | Lorsqu’il est défini, le protocole IPX effectue une somme de contrôle sur les paquets sortants et vérifie la somme de contrôle des paquets entrants. Non pris en charge sur toutes les plateformes.                          |
| \_TXPKTSIZE SPX   | int  | Taille du média à un maximum de 1466 | Définit la taille maximale du datagramme d’envoi. Cette taille n’inclut pas l’en-tête SPX ni les en-têtes de support qui peuvent également être utilisés. Peut être augmentée à la taille du média.    |
| \_RXPKTSIZE SPX   | int  | Taille du média à un maximum de 1466 | Définit la taille maximale de datagramme de réception. Cette taille n’inclut pas l’en-tête SPX ni les en-têtes de support qui peuvent également être utilisés. Peut être augmentée à la taille du média. |
| \_TXMEDIASIZE SPX | int  | Tableau principal                   | Retourne la taille du média d’envoi moins les en-têtes SPX et Media. Cela définit une limite supérieure pour la taille du paquet de segmentation de message.                                       |
| \_RXMEDIASIZE SPX | int  | Tableau principal                   | Retourne la taille du média de réception moins les en-têtes SPX et Media. Cela définit une limite supérieure pour la taille des paquets de réception.                                                 |
| \_RAWSPX SPX      | Bool | arrêt                             | Lorsque cette valeur est définie, l’en-tête du protocole IPX/SPX est transmis avec les données.                                                                                                |



 

## <a name="remarks"></a>Remarques

Les options de socket **\_ IPX NSPROTO** et les structures utilisées par ces options de socket sont définies dans le fichier d’en-tête *Wsnwlink. h* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wsnwlink. h</dt> </dl> |



 

 




