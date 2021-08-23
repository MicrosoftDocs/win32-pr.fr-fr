---
description: 'L’API de regroupement utilise les fonctions suivantes :'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Fonctions d’API de regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 888a64096f66a9adf048d91c2d577d71203a03da6d1b698f2ea305396c4be0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776169"
---
# <a name="grouping-api-functions"></a>Fonctions d’API de regroupement

L’API de regroupement utilise les fonctions suivantes :

## <a name="group-initialization-and-cleanup-functions"></a>Fonctions d’initialisation et de nettoyage des groupes



| Fonction                                       | Description                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Ferme un groupe homologue créé avec [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) et supprime toutes les ressources allouées. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Initie un groupe homologue à l’aide d’une version demandée de l’infrastructure homologue.                                        |



 

## <a name="group-creation-and-access-functions"></a>Fonctions de création de groupe et d’accès



| Fonction                                                                       | Description                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Invalide le descripteur du groupe homologue obtenu par un appel précédent à la fonction [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) . |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Lance une recherche PNRP pour un groupe homologue et tente de s’y connecter. Une fois que cette fonction a été appelée avec succès, un homologue peut communiquer avec les autres membres du groupe homologue.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Tente de se connecter au groupe homologue auquel les autres pairs avec des adresses IPv6 connues participent.                                                                                                       |
| [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Crée un nouveau groupe homologue.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Retourne une chaîne XML qui peut être utilisée par l’homologue spécifié pour joindre un groupe.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Retourne une chaîne XML qui peut être utilisée par l’homologue spécifié pour joindre un groupe avec un mot de passe correspondant.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Supprime les données locales et le certificat associé à un groupe homologue.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Récupère l’état actuel d’un groupe.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Émet des informations d’identification, y compris un GMC, vers une identité spécifique et retourne éventuellement une chaîne XML d’invitation que l’homologue invité peut utiliser pour joindre un groupe homologue.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Permet à un homologue avec une invitation de joindre un groupe homologue existant.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Ouvre un groupe homologue qu’un homologue a créé ou joint.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Retourne une structure d' [**\_ \_ informations d’invitation de pairs**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) avec les détails d’une invitation spécifique.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Permet à un homologue disposant d’une invitation et du mot de passe correct de rejoindre un groupe homologue protégé par mot de passe.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Fonctions d’informations de groupe et de membre



| Fonction                                                 | Description                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Crée une énumération des membres du groupe homologue disponibles et des informations d’appartenance associées.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Récupère des informations sur les propriétés d’un groupe spécifié.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Définit les propriétés actuelles du groupe homologue. Dans la version 1,0 de cette API, seul le créateur du groupe homologue peut effectuer cette opération. |



 

## <a name="records-and-record-management-functions"></a>Fonctions de gestion des enregistrements et des enregistrements



| Fonction                                                 | Description                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Ajoute un nouvel enregistrement au groupe homologue, qui est propagé à tous les homologues participants. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Supprime un enregistrement d’un groupe homologue. Seul le créateur d’un enregistrement peut le supprimer.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Crée une énumération des enregistrements du groupe homologue.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Récupère un enregistrement de groupe spécifique.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Recherche dans la base de données du groupe homologue local les enregistrements qui correspondent aux critères fournis. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Met à jour un enregistrement dans un groupe homologue spécifique.                                       |



 

## <a name="group-database-importexport-functions"></a>fonctions de Import/Export de base de données de groupe



| Fonction                                                   | Description                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exporte une base de données de groupe homologue dans un fichier spécifique, qui peut être transporté vers un autre ordinateur et importé avec la fonction [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) . |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importe une base de données de groupe homologue à partir d’un fichier local.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Fonctions de connexion directe



| Fonction                                                                 | Description                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Ferme une connexion directe spécifique entre deux homologues.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Crée une énumération des connexions actuellement actives sur l’homologue. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Établit une connexion directe avec un autre homologue dans un groupe homologue.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Envoie des données à un membre via un voisin ou une connexion directe.        |



 

## <a name="group-events-infrastructure"></a>Infrastructure des événements de groupe



| Fonction                                                     | Description                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Permet à une application de récupérer les données retournées par un événement de regroupement.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Inscrit un homologue pour des événements de groupe homologue spécifiques.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Annule l’inscription d’un homologue de la notification d’événements homologues associée au handle d’événement fourni. |



 

## <a name="group-time-conversion-functions"></a>Fonctions de conversion de temps de groupe



| Fonction                                                                     | Description                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Convertit la valeur de temps de référence gérée du groupe homologue en une valeur de temps localisée appropriée pour l’affichage sur un ordinateur homologue. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Convertit une valeur d’heure locale de l’ordinateur d’un homologue en une valeur de temps de groupe pair commune.                                         |



 

## <a name="group-configuration-functions"></a>Fonctions de configuration de groupe



| Fonction                                               | Description                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exporte la configuration de groupe pour un homologue sous la forme d’une chaîne XML qui contient l’identité, le nom du groupe et le GMC pour l’identité. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importe une configuration de groupe homologue pour une identité basée sur les paramètres spécifiques d’une chaîne de configuration XML fournie.         |



 

 

 



