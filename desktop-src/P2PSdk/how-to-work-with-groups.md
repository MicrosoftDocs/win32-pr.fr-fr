---
description: Le regroupement d’égal à égal est une technologie qui permet à un développeur de créer un réseau pair à pair sécurisé rapidement et efficacement.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Utilisation des groupes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009240"
---
# <a name="how-to-work-with-groups"></a>Utilisation des groupes

Le regroupement d’égal à égal est une technologie qui permet à un développeur de créer un réseau pair à pair sécurisé rapidement et efficacement. La liste suivante identifie les principales considérations à prendre en compte lors de la création d’une application de regroupement pair.

-   [Obtention d’une identité d’homologue](#obtaining-a-peer-identity)
-   [Démarrage d’un groupe homologue](#starting-up-the-peer-grouping-infrastructure)
-   [Inscription pour les événements de regroupement](#registering-for-peer-grouping-events)
-   [Connexion à un groupe](#obtaining-a-group-handle)
-   [Création de rôles d’administrateur et de membre](#creating-administrator-and-member-roles)
-   [Recherche d’un homologue](#finding-a-peer)
-   [Connexion directe à un homologue](#connecting-directly-to-a-peer)
-   [Fermeture et arrêt d’un groupe](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Obtention d’une identité d’homologue

Avant de créer ou de vous connecter à un groupe, un homologue doit obtenir une identité d’homologue, qui est un nom utilisé pour identifier de manière unique un pair à un groupe. Pour obtenir une liste énumérée de toutes les identités d’homologue définies sur l’homologue, appelez [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), qui retourne un handle vers l’énumération. Pour obtenir les identités d’homologue, appelez [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) avec le handle d’énumération et le nombre de membres à récupérer. Poursuivez l’appel de **PeerGetNextItem** jusqu’à ce que le paramètre *pCount* retourne une valeur inférieure au nombre d’identités d’homologues demandées.

Si une identité d’homologue pour l’homologue n’existe pas, elle peut être créée en appelant [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Après la création d’une identité d’homologue, l’homologue génère un objet BLOB XML d’identité qui contient la clé publique qui lui est assignée.

Les informations d’identité de l’homologue sont obtenues en appelant [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml). Les informations d’identité de l’homologue sont utilisées par le créateur du groupe ou un administrateur pour émettre les informations d’identification nécessaires pour joindre le groupe, en tant qu’objet BLOB XML d’invitation.

Pour plus d’informations sur les identités d’homologues, consultez la documentation de l' [API Identity Manager](identity-manager-api.md) .

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Démarrage de l’infrastructure de regroupement d’homologues

Avant qu’une fonction de l’API de regroupement pair ne soit appelée par une application, [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) doit être appelé. Cette fonction initialise l’infrastructure de regroupement de pairs pour l’application et définit la version prise en charge.

## <a name="obtaining-a-group-handle"></a>Obtention d’un descripteur de groupe

Pour vous connecter à un groupe et commencer à participer, vous devez obtenir un handle vers un groupe homologue. La liste suivante identifie les trois manières de se connecter à un groupe homologue :

-   Création d’un groupe homologue en appelant [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), qui initialise un nouveau groupe homologue et retourne un handle valide avec l’homologue comme propriétaire et administrateur unique.
-   Joindre un groupe homologue en appelant [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Pour joindre un groupe homologue, un homologue doit recevoir une invitation d’un administrateur de groupe homologue. Pour obtenir une invitation, envoyez l’objet BLOB XML des informations d’identité à l’administrateur qui crée une invitation et vous l’envoie par un mécanisme externe, tel que la messagerie électronique ou FTP. L’invitation et l’identité de l’homologue sont passées à **PeerGroupJoin**, qui retourne un handle valide pour le groupe.
-   Ouverture d’un groupe homologue qu’un homologue a rejoint précédemment en appelant [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). Dans ce cas, l’obtention d’une invitation n’est pas nécessaire.

Une fois que vous avez obtenu un handle de groupe homologue valide à partir de l’une des fonctions ci-dessus, vous pouvez vous connecter à un groupe homologue en appelant [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) avec le nouveau handle.

> [!Note]  
> Si la connexion à un groupe homologue échoue, l’événement échec de la connexion à un événement de groupe HOMOLOGUe \_ \_ \_ \_ se produit. Le gestionnaire peut tenter de rétablir la connexion au groupe homologue.

 

## <a name="registering-for-peer-grouping-events"></a>Inscription pour les événements de regroupement d’homologues

Avant qu’un homologue ne participe à un groupe homologue, l’homologue doit s’inscrire pour les événements de groupe homologue. Pour s’inscrire à des événements homologues spécifiques, appelez [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)et transmettez un ou plusieurs des types d’événements homologues définis dans \_ type d’événement de groupe pair \_ \_ . Vous devez vous inscrire pour chaque événement homologue qui s’applique à votre application. par exemple, pour recevoir des données via une connexion directe, inscrivez-vous \_ aux \_ événements de connexion directe d’événement de groupe pair \_ et de \_ \_ \_ \_ données entrantes d’événement de groupe pair \_ . Chaque appel prend un handle d’événement et retourne un handle **HPEEREVENT** pour cet événement homologue.

Les gestionnaires d’événements peuvent obtenir les données associées à un événement homologue en passant le handle aux événements homologues inscrits dans [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Ces données d’événement homologues sont retournées sous la forme d’une Union de données d’événement de groupe HOMOLOGUe \_ \_ \_ . Si la file d’attente d’événements homologues est vide, cette fonction retourne l’HOMOLOGUe \_ S \_ sans \_ données d’événement \_ .

Vous pouvez annuler l’inscription des événements homologues en appelant [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) et en fournissant le descripteur de l’événement homologue dont vous souhaitez annuler l’inscription. Une fois la fonction appelée, les événements homologues associés au descripteur ne sont plus inscrits.

## <a name="creating-administrator-and-member-roles"></a>Création de rôles d’administrateur et de membre

L’homologue qui crée le groupe homologue est appelé le créateur du groupe homologue et possède le rôle administrateur par défaut. Seul le créateur du groupe homologue peut définir les propriétés du groupe.

Les pairs invités au groupe homologue peuvent être un administrateur ou un membre. S’ils se voient attribuer un rôle d’administrateur par l’administrateur émettant l’invitation, ils peuvent inviter de nouveaux membres sur le groupe homologue, et également attribuer le rôle d’administrateur à d’autres membres.

Les rôles des membres du groupe homologue sont définis dans les invitations que l’administrateur donne à un membre. Pour ajouter d’autres administrateurs, définissez la valeur du paramètre *pRoles* de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) sur administrateur de rôle de groupe homologue lors de la \_ \_ \_ création d’une invitation.

Les membres peuvent participer à un groupe homologue, mais ils ne peuvent pas inviter et autoriser de nouveaux membres, définir des propriétés de groupe ou mettre à jour ou supprimer des enregistrements de groupe qu’ils ne créent pas spécifiquement. Pour affecter l’état d’un membre à un homologue participant, définissez la valeur du paramètre **pRoles** de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) sur le membre du rôle de groupe homologue \_ \_ \_ lorsque vous créez une invitation pour cet homologue.

Pour modifier le rôle d’un membre, les nouvelles informations d’identification contenant le nouveau rôle doivent être délivrées à ce membre. Pour ce faire, obtenez la structure des [**\_ \_ informations d’identification de l’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) pour ce membre à partir de la structure de membre homologue \_ retournée par [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Remplacez le champ **pRoles** dans **\_ \_ informations d’identification de l’homologue** par le nouveau rôle et passez la structure à [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Les nouvelles informations d’identification n’entrent pas en vigueur pour l’homologue jusqu’à ce qu’elles se connectent au groupe homologue. S’ils sont actuellement connectés, ils doivent fermer le groupe et se reconnecter pour obtenir les informations d’identification mises à jour.

## <a name="finding-a-peer"></a>Recherche d’un homologue

Pour obtenir une liste énumérée de tous les pairs qui participent au groupe pair, appelez [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) avec le descripteur de groupe, qui retourne un handle à l’énumération. Pour obtenir les membres, appelez [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) avec le handle enum et le nombre de membres à récupérer. Continue d’appeler **PeerGetNextItem** jusqu’à ce que le paramètre *pCount* retourne une valeur inférieure au nombre de membres demandés. Notez que la liste complète des membres disponibles ne peut pas être retournée.

Chaque membre est représenté sous la forme d’une structure de [**\_ membre homologue**](/windows/desktop/api/P2P/ns-p2p-peer_member) , qui contient l’identité de l’homologue, les ID de nœud et les adresses IP des homologues actifs.

Lorsque vous avez terminé, fermez l’énumération et libérez la mémoire associée en appelant [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Connexion directe à un homologue

Lorsqu’un homologue est connecté à un groupe homologue, les échanges de type un-à-un avec d’autres membres connectés sont initiés en appelant [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) et en fournissant l’identité de l’autre homologue. Cet appel est asynchrone et retourne un ID de connexion 64 bits. Si l’appel réussit, vous recevez l' \_ \_ \_ \_ \_ événement homologue d’événement de connexion directe d’événement de groupe homologue pour indiquer que la connexion a réussi. Si la connexion réussit, l’ID de connexion est valide et peut être utilisé pour envoyer et recevoir des données via la connexion directe.

Pour pouvoir recevoir des connexions directes, l’autre homologue doit également avoir été précédemment inscrit pour l' \_ \_ événement d' \_ homologue de connexion directe d’événement de groupe pair \_ .

Pour envoyer des données à un homologue, appelez [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) avec un ID de connexion valide. Pour recevoir des données, l’autre homologue doit être inscrit pour \_ l' \_ \_ \_ événement homologue des données entrantes de l’événement de groupe homologue. De même, si l’homologue expéditeur souhaite recevoir des données à son tour, il doit également être inscrit pour l' \_ \_ \_ \_ événement homologue des données entrantes de l’événement de groupe homologue.

Pour recevoir le jeu total de connexions directes actuellement actives avec d’autres pairs dans un groupe, appelez [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) pour ouvrir l’énumération et itérer dans la liste des connexions à l’aide de [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Pour fermer une connexion directe, appelez [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) et transmettez l’ID de connexion.

## <a name="closing-and-shutting-down-a-peer-group"></a>Fermeture et arrêt d’un groupe homologue

Pour fermer une connexion à un groupe homologue, appelez [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), qui invalide le descripteur de groupe, mais n’arrête pas l’infrastructure de regroupement d’homologues. Les données de groupe d’égal à égal sont supprimées en appelant [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Lorsque l’application a terminé d’utiliser l’infrastructure de regroupement d’homologues, elle doit appeler [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



