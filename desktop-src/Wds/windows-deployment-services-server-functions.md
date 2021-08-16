---
title: Windows Fonctions du serveur des services de déploiement
description: les fonctions suivantes sont utilisées avec Windows API du serveur de déploiement PXE.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cc99f01dc88fce91beafe51a65f8e8ddccfdf08c4361fb194a7e60451a5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330602"
---
# <a name="windows-deployment-services-server-functions"></a>Windows Fonctions du serveur des services de déploiement

les fonctions suivantes sont utilisées avec Windows API du serveur de déploiement PXE.



| Fonction                                                           | Description                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Retourne les résultats asynchrones de la requête du client.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Ajoute une option DHCP au paquet de réponse.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Ajoute une option DHCP au paquet de réponse.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Récupère une valeur d’option à partir d’un paquet DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Récupère une valeur d’option à partir du champ d’informations spécifiques au fournisseur (43) d’un paquet DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Initialise un paquet de réponse en tant que paquet de réponse DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Valide le fait qu’un paquet soit un paquet DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Retourne des informations sur le serveur PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Alloue un paquet à envoyer avec la fonction [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) .                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libère un paquet alloué par la fonction [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) .                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Ferme l’énumération des fournisseurs ouverts par la fonction [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) .               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Démarre une énumération des fournisseurs inscrits.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Énumère les fournisseurs inscrits.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libère la mémoire allouée par la fonction [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) .                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Retourne l’index du fournisseur spécifié dans la liste des fournisseurs inscrits.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Appelée lorsqu’une demande est reçue d’un client.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Inscrit un fournisseur auprès du système.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Appelée lorsqu’un code de contrôle de service est reçu par le service WDS.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Spécifie les attributs du fournisseur.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Appelé pour arrêter le fournisseur.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Supprime un fournisseur de la liste des fournisseurs inscrits.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Inscrit des fonctions de rappel pour différents événements de notification.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Envoie un paquet à une demande du client.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Ajoute une entrée de trace au Journal PXE.                                                                                             |



 

les éléments suivants sont disponibles à partir de Windows 8 et Windows Server 2012.

| Fonction                                                               | Description                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Ajoute une option DHCPv6 au paquet de réponse.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Ajoute une option DHCPv6 au paquet de réponse.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Récupère une valeur d’option à partir d’un paquet DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Récupère les valeurs d’option du \_ champ option Vendor \_ OPTS (17) d’un paquet DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Initialise un paquet de réponse en tant que paquet de réponse DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Valide le fait qu’un paquet soit un paquet DHCPv6 valide.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Retourne des informations sur le serveur PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Permet à un fournisseur d’analyser les messages RELAY-FORW et leurs messages de message de relais d’OPTION imbriqués \_ \_ . |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Génère un message de réplication de relais.                                                               |



 

 

 




