---
description: NLA est en charge de fournir à ses clients la notification des modifications d’emplacement réseau. Le mécanisme utilisé pour demander la notification des événements de modification est une combinaison des fonctions WSALookupServiceBegin, WSANSPIoctl et WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notification de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526127"
---
# <a name="notification-from-nla"></a>Notification de NLA

NLA est en charge de fournir à ses clients la notification des modifications d’emplacement réseau. Le mécanisme utilisé pour demander la notification des événements de modification est une combinaison des fonctions [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)et [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

Pour recevoir une notification de modification d’NLA, un client doit d’abord appeler [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) pour obtenir un handle de recherche NLA SP valide. Ensuite, le client peut appeler [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) ou [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) dans n’importe quel ordre ; pour vous inscrire à la notification, appelez la fonction **WSANSPIoctl** avec \_ l' \_ ensemble de codes de \_ contrôle de modification de la NSP SIO dans le paramètre *dwControlCode* .

La fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retourne le WSA \_ E plus \_ \_ comme délimiteur défini. Lorsqu’un client s’est inscrit à la notification à l’aide de la fonction [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) et que **WSALOOKUPSERVICENEXT** retourne \_ un WSA E \_ \_ plus, l’appel de **WSALookupServiceNext** indique si une modification a eu lieu :

-   Si aucune modification n’a eu lieu depuis le WSA précédent \_ e \_ , le \_ WSA \_ e \_ n' \_ est pas retourné.
-   Si une modification est apportée, ou si une modification s’est produite et un appel d’interrogation, l’appel de fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retourne des réseaux en tant que structures [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , avec l’un des indicateurs suivants définis dans son membre **dwOutputFlags** :

    <dl> le résultat \_ est \_ ajouté  
    RÉSULTAT \_ \_ modifié  
    le résultat \_ est \_ supprimé  
    </dl>

La notification de modification est fournie pour tous les champs qui ont été modifiés depuis l’obtention du handle de recherche NLA avec l’appel de fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) , ou depuis la dernière énumération qui a provoqué l’erreur du WSA \_ E \_ \_ . Lorsque toutes les informations d’emplacement réseau modifiées sont fournies, le WSA \_ E n' \_ \_ est pas retourné. Les clients peuvent réémettre un appel de fonction [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) sur le même handle de requête à tout moment, l’un après l’autre, avec l' \_ indicateur de changement de notification NSP SIO \_ \_ défini. Cette fonctionnalité permet à un client de recycler le descripteur de requête en continu, ce qui évite au client d’avoir à gérer les informations d’état de modification de manière autonome. Une fois qu’un client n’a plus besoin de notifications de modifications, il doit fermer le descripteur de requête à l’aide de la fonction [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

 

 



