---
title: Fonctions de transport serveur et station de travail
description: Le serveur de gestion de réseau et les fonctions de transport de station de travail gèrent la liaison et la dissociation des protocoles de transport vers et à partir du serveur et du redirecteur.
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517951"
---
# <a name="server-and-workstation-transport-functions"></a>Fonctions de transport serveur et station de travail

Le serveur de gestion de réseau et les fonctions de transport de station de travail gèrent la liaison et la dissociation des protocoles de transport vers et à partir du serveur et du redirecteur. Les fonctions de transport de serveur traitent des protocoles de transport gérés par le serveur. les fonctions de transport de station de travail traitent des protocoles de transport gérés par le redirecteur.

Le partage de fichiers entre un périphérique de transport et un serveur comporte deux composants :

-   Ordinateur serveur sur lequel les fichiers résident
-   Un client SMB (Server Message Block) qui accède aux fichiers

L’ordinateur client communique avec l’ordinateur serveur sur un réseau local à l’aide d’un protocole de transport. par exemple, TCP ou XNS. Le client envoie des demandes au serveur pour récupérer des données. Le logiciel sur l’ordinateur client qui génère les demandes de fichier s’appelle le *redirecteur* , car il redirige les demandes de fichier local vers l’ordinateur serveur. Le logiciel sur l’ordinateur qui reçoit et agit sur les demandes de fichier est appelé *serveur* , car il dessert les clients. Le format spécifique à ces demandes est appelé le protocole SMB.

Les fonctions de transport de serveur sont répertoriées ci-après.



| Fonction                                                     | Description                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Lie un nom de serveur émulé à chacun des protocoles de transport sur lesquels un serveur est actif. (Combine les fonctionnalités de la fonction [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) et de la fonction [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) .)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Déconnecte chaque protocole de transport réseau d’un nom de serveur émulé défini par un appel précédent à la fonction **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Lie le serveur spécifié au protocole de transport. (Cette fonction prend en charge uniquement le niveau d’information [**Server \_ transport \_ information \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) .)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Lie le serveur spécifié au protocole de transport. (Cette fonction étendue prend en charge les niveaux d’information Server transport information [**\_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ transport \_ information \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)et [**Server \_ transport \_ information \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Déconnecte le protocole de transport du serveur.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Énumère les protocoles de transport gérés par le serveur.                                                                                                                                                                                                                                                                   |



 

Les fonctions de transport serveur sont disponibles aux niveaux d’informations suivants :

-   [**\_Informations sur le transport serveur \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**\_Informations sur le transport serveur \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**\_Informations sur le transport serveur \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**\_Informations sur le transport serveur \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

Les fonctions de transport de station de travail effectuent des opérations équivalentes pour la station de travail.

**Windows Server 2003 et Windows XP/2000 :** Le redirecteur ne prend pas en charge la fonction [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) ou la fonction [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) . Vous pouvez modifier manuellement les paramètres par défaut des protocoles de transport via la boîte de dialogue **Propriétés de connexion** au réseau local dans le dossier **connexions réseau et accès à distance** .

Les fonctions de transport de station de travail sont répertoriées ci-dessous.



| Fonction                                               | Description                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | Connecte le redirecteur au protocole de transport.                |
| [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | Déconnecte le protocole de transport du redirecteur.           |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | Répertorie les protocoles de transport qui sont gérés par le redirecteur. |



 

Les fonctions de transport de station de travail sont disponibles à un niveau d’information :

-   [**WKSTA \_ transport \_ info \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




