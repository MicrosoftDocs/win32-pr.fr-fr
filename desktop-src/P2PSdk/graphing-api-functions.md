---
description: 'L’API de représentation graphique d’homologue utilise les fonctions suivantes :'
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Fonctions de l’API Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26c40770e8fcbc18b08ccb73dcfea5f1f6c4eab65be615ed76d8088ddc90954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776219"
---
# <a name="graphing-api-functions"></a>Fonctions de l’API Graph

L’API de représentation graphique d’homologue utilise les fonctions suivantes :

## <a name="initialization-and-cleanup-functions"></a>Fonctions d’initialisation et de nettoyage



| Fonction                                       | Description                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Nettoie toutes les ressources allouées par l’appel à [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup).                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Indique à l’infrastructure de représentation graphique des homologues la version des protocoles homologues requise par l’application appelante. |



 

## <a name="graph-creation-and-access-functions"></a>Graph Fonctions de création et d’accès



| Fonction                                   | Description                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Invalide le handle de graphique homologue retourné par un appel à [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) ou [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen), et ferme toutes les connexions réseau pour le graphique homologue spécifié. |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Crée un graphique homologue.                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Supprime les données associées à un graphique homologue spécifié.                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Indique qu’un graphique homologue doit commencer à écouter les connexions entrantes.                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Ouvre un graphique homologue créé précédemment par le nœud local ou un nœud distant.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>fonctions d’informations de Graph et de nœud



| Fonction                                                         | Description                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Crée et retourne un handle d’énumération utilisé pour énumérer les nœuds dans un graphique homologue.                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Récupère des informations sur un nœud spécifique.                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Récupère les propriétés du graphique homologue actuel.                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Retourne l’état actuel du graphique homologue.                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Définit les attributs de la structure d' [**\_ \_ informations du nœud homologue**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) pour le nœud local.                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Active ou désactive explicitement la publication des enregistrements de présence pour un nœud spécifique. Cette fonction peut remplacer les paramètres de présence dans les propriétés du graphique homologue. |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Définit les propriétés du graphique homologue.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Fonctions de gestion des enregistrements



| Fonction                                                                     | Description                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Ajoute un nouvel enregistrement à un graphique homologue. Un enregistrement ajouté avec cette fonction est envoyé à chaque nœud dans un graphique homologue.                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Marque un enregistrement comme supprimé dans un graphique homologue.                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Crée et retourne un handle d’énumération utilisé pour énumérer les enregistrements d’un type spécifique d’enregistrement, d’utilisateur ou des deux.                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Récupère un enregistrement spécifique en fonction de l’ID d’enregistrement spécifié.                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Recherche des enregistrements spécifiques dans le graphique homologue.                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Met à jour un enregistrement dans le graphique d’homologue, puis sature l’enregistrement à chaque nœud dans le graphique d’homologue.                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Indique à l’infrastructure de représentation graphique des homologues qu’il est temps de soumettre à nouveau tous les enregistrements différés pour le module de sécurité à valider. |



 

## <a name="export-and-import-functions"></a>Fonctions d’exportation et d’importation



| Fonction                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Exporte une base de données de graphiques homologues dans un fichier que vous pouvez déplacer vers un autre ordinateur. |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importe un fichier qui contient les informations d’une base de données de graphiques homologues.             |



 

## <a name="utility-and-support-functions"></a>Fonctions de l’utilitaire et de la prise en charge



| Fonction                                                                     | Description                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Libère un handle d’énumération et libère les ressources associées à une énumération.                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Libère les ressources retournées par plusieurs fonctions d’API graphiques d’homologues.                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Récupère le nombre d’éléments d’une énumération.                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Obtient le ou les éléments suivants dans une énumération créée par un appel à des fonctions spécifiques, qui retournent une énumération homologue.        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Convertit la valeur de temps de référence gérée par graphique de l’homologue en une valeur de temps localisée appropriée pour l’affichage sur l’ordinateur de l’homologue. |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Convertit une valeur de temps universel de l’ordinateur de l’homologue en une valeur d’heure de graphique d’homologue commune.                                       |



 

## <a name="connection-functions"></a>Fonctions de connexion



| Fonction                                                                 | Description                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Ferme une connexion directe spécifiée.                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Tente d’établir une connexion à un nœud spécifié dans un graphique homologue. Cette fonction démarre une opération asynchrone.                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Crée et retourne un handle d’énumération utilisé pour énumérer les connexions d’un nœud local.                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Permet à une application d’établir une connexion directe avec un nœud dans un graphique homologue. La connexion peut être établie uniquement si le nœud auquel l’application se connecte s’est abonné à l’événement de **\_ \_ \_ \_ connexion directe d’événement de graphique pair à pair** . |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Envoie des données à un nœud voisin ou directement connecté.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Fonctions d’infrastructure des événements



| Fonction                                                     | Description                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Récupère les événements homologues.                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Inscrit la demande d’un homologue pour être averti des modifications associées à un graphique homologue et à un type d’événement.            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Demande que l’application ne soit plus avertie des modifications associées à un graphique homologue et un type d’enregistrement. |



 

 

 



