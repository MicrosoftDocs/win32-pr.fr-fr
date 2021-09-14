---
description: Le tableau suivant décrit les \_ options de socket RM IPPROTO qui s’appliquent aux sockets créés pour la famille d’adresses IPv4 (AF \_ inet) avec le paramètre de protocole à la fonction de socket spécifiée comme Reliable multicast (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: Options de socket IPPROTO_RM (WSRM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292079"
---
# <a name="ipproto_rm-socket-options"></a>\_Options de socket RM IPPROTO

Le tableau suivant décrit les options de socket **\_ RM IPPROTO** qui s’appliquent aux sockets créés pour la famille d’adresses IPv4 (AF \_ inet) avec le paramètre de *protocole* à la fonction de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) spécifiée comme Reliable multicast (IPPROTO \_ RM). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

**Windows XP :** La programmation de la multidiffusion (PGM) fiable n’est pas prise en charge.

Certaines options de socket requièrent plus d’explications que celles pouvant être transmises par ces tables. ces options contiennent des liens vers des pages supplémentaires.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**\_Options de socket RM IPPROTO**</dt> <dd> <dl> <dt> 

| Option                              | Obtenir | Définissez | Type Optval                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM- \_ Ajouter une \_ réception \_ si                |     | Oui | ULONG                                            | Récepteur uniquement. Ajoute une interface sur laquelle écouter (la valeur par défaut est la première interface locale énumérée). Le paramètre optval spécifie l’interface réseau dans l’ordre d’octet du réseau à ajouter. La valeur spécifiée remplace l’interface par défaut sur le premier appel d’un socket donné et ajoute d’autres interfaces lors des appels suivants. Pour obtenir \_ un comportement inaddr, chaque interface réseau doit être ajoutée séparément. |
| \_réception RM \_ del \_ si                |     | Oui | ULONG                                            | Récepteur uniquement. Supprime une interface ajoutée à l’aide de RM \_ Add \_ Receive \_ si. Le paramètre optval spécifie l’interface réseau dans l’ordre d’octet du réseau à supprimer.                                                                                                                                                                                                                                                            |
| \_FLUSHCACHE RM                      |     | Oui | N/A                                              | Non implémenté.                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_ \_ abonnement intranet à vitesse élevée \_ RM \_      | Oui | Oui | ULONG                                            | Récepteur uniquement. Spécifie si une connexion LAN à bande passante élevée (100 Mbits/s) est utilisée.                                                                                                                                                                                                                                                                                                                                   |
| \_LATEJOIN RM                        | Oui | Oui | ULONG                                            | Expéditeur uniquement. Pourcentage de la taille de fenêtre pouvant être demandée par les récepteurs de jointure tardive lors de l’acceptation de la session. La valeur maximale est 75% (la valeur par défaut est zéro). Désactivez ce paramètre en appelant à nouveau avec la valeur définie sur zéro.                                                                                                                                                                                                |
| taille de la \_ fenêtre de tarif RM \_ \_              | Oui | Oui | [**\_fenêtre d’envoi RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Expéditeur uniquement. Définit la limite du taux de transmission, la durée d’avancement de la fenêtre et la taille de la fenêtre.                                                                                                                                                                                                                                                                                                                                   |
| \_statistiques du récepteur RM \_            | Oui |     | [**\_statistiques du récepteur RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Récepteur uniquement. Récupère les statistiques pour la session réceptrice.                                                                                                                                                                                                                                                                                                                                                         |
| taux d’avancée de la \_ fenêtre d’envoi RM \_ \_ \_         | Oui | Oui | ULONG                                            | Expéditeur uniquement. Spécifie le taux d’avance incrémentale pour la fenêtre d’envoi du bord de fin (la valeur par défaut est 15%). La valeur maximale est de 50%.                                                                                                                                                                                                                                                                                          |
| \_statistiques des expéditeurs RM \_              | Oui |     | [**statistiques de l' \_ expéditeur RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Expéditeur uniquement. Récupère des statistiques pour la session d’envoi.                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ méthode avancée de la fenêtre d’expéditeur RM \_ | Oui | Oui | ULONG                                            | Expéditeur uniquement. Le paramètre optval spécifie la méthode utilisée lors de l’avancement de la fenêtre d’envoi du bord de fin. Le paramètre optval peut uniquement être une \_ fenêtre \_ Advance \_ par \_ heure (valeur par défaut). Notez que l' \_ \_ utilisation \_ du cache de données par la fenêtre E \_ \_ n’est pas prise en charge.                                                                                                                                                                     |
| RM \_ Set \_ MCAST \_ TTL                 |     | Oui | ULONG                                            | Expéditeur uniquement. Définit le paramètre de durée de vie maximal pour les paquets de multidiffusion. La valeur maximale et la valeur par défaut est 255.                                                                                                                                                                                                                                                                                                      |
| configuration de la \_ \_ limite du message RM \_          |     | Oui | ULONG                                            | Expéditeur uniquement. Spécifie la taille du message suivant à envoyer, en octets. Significatif uniquement pour les sockets en mode message (RDM de chaussette \_ ). Peut être défini pendant que la session est en cours.                                                                                                                                                                                                                                                |
| RM- \_ définir \_ Envoyer \_ si                   | Oui | Oui | ULONG                                            | Expéditeur uniquement. Définit l’adresse IP de l’interface d’envoi dans l’ordre des octets du réseau.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ utiliser \_ FEC                        | Oui | Oui | [**\_informations FEC \_ RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Expéditeur uniquement. Indique à l’expéditeur d’appliquer les techniques de correction des erreurs de transfert pour envoyer des données de réparation. FEC a trois modes : paquets de parité pro-actif uniquement, paquets de parité à la demande uniquement, ou les deux. Pour plus d’informations, consultez structure des [**\_ \_ informations FEC sur RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) .                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows Prise en charge des \_ options RM IPPROTO**</dt> <dd> <dl> <dt> 

| Option                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows 4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM- \_ Ajouter une \_ réception \_ si                | x         | x                   | x             | x                   | x          |              |             |               |
| \_réception RM \_ del \_ si                | x         | x                   | x             | x                   | x          |              |             |               |
| \_FLUSHCACHE RM                      | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ abonnement intranet à vitesse élevée \_ RM \_      | x         | x                   | x             | x                   | x          |              |             |               |
| \_LATEJOIN RM                        | x         | x                   | x             | x                   | x          |              |             |               |
| taille de la \_ fenêtre de tarif RM \_ \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_statistiques du récepteur RM \_            | x         | x                   | x             | x                   | x          |              |             |               |
| taux d’avancée de la \_ fenêtre d’envoi RM \_ \_ \_         | x         | x                   | x             | x                   | x          |              |             |               |
| \_statistiques des expéditeurs RM \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ \_ méthode avancée de la fenêtre d’expéditeur RM \_ | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ Set \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| configuration de la \_ \_ limite du message RM \_          | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ définir \_ Envoyer \_ si                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ utiliser \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les options de socket **\_ RM IPPROTO** et les structures utilisées par ces options de socket sont définies dans le fichier d’en-tête *wsrm. h* .

La constante **\_ PGM** **IPPROTO \_ RM** ou IPPROTO peut être utilisée pour spécifier le paramètre de *protocole* à la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) afin d’utiliser les options de socket RM. sur le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, la constante **\_ PGM IPPROTO** est définie dans le fichier d’en-tête *Ws2def. h* sur la même valeur que la constante **\_ RM IPPROTO** définie dans le fichier d’en-tête *Wsrm. h* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WSRM. h</dt> </dl> |



 

 




