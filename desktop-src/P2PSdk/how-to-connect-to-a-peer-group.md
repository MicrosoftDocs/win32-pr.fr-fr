---
description: Cette rubrique explique comment une application se connecte à un groupe homologue à l’aide des API de regroupement pair.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: comment Connecter à un groupe homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009244"
---
# <a name="how-to-connect-to-a-peer-group"></a>comment Connecter à un groupe homologue

Cette rubrique explique comment une application se connecte à un groupe homologue à l’aide des API de regroupement pair.

## <a name="joining-a-peer-group"></a>Joindre un groupe homologue

Pour joindre un groupe homologue, appelez [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), en transmettant le nom d’identité de l’homologue et de l’invitation (et un nom de Cloud PNRP facultatif, si le nom du Cloud dans l’invitation est ambigu).

En cas de réussite, [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) retourne un handle vers le groupe homologue.

Si l’homologue a déjà rejoint le groupe homologue, puis fermé le handle, le groupe homologue doit être rouvert en appelant [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) et en passant le nom du groupe homologue. Cet appel retourne un nouveau handle de groupe homologue.

Une fois le groupe homologue correctement joint, l’homologue peut se connecter directement au groupe homologue et commencer à interagir en appelant [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Une fois connecté, l’homologue est considéré comme « en ligne ».

Si une application n’interagit pas avec le groupe à ce moment-là, elle peut rester « hors connexion ». S’il choisit de participer directement au groupe homologue dans une instance ultérieure, un appel ultérieur à [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) le met en ligne. Une fois qu’un homologue a rejoint le groupe homologue, il doit se connecter au moins une fois avant de pouvoir publier des enregistrements dans le groupe homologue.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Ouverture d’un groupe homologue sans connexion (hors connexion)

Souvent, vous souhaiterez peut-être que l’application se connecte à un groupe pair, mais ne la participe pas directement, en recevant et en publiant des mises à jour d’enregistrement, mais pas en envoyant ou en recevant des messages de données. Une application est dans cet État « hors connexion » immédiatement après l’appel de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .

Une application hors connexion peut être mise en ligne à tout moment en appelant [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Une fois connecté, un groupe homologue ne peut pas passer en mode hors connexion jusqu’à ce que toutes les autres applications associées à cette identité et partageant ce groupe y aient également fermé des connexions.

Un groupe homologue est une ressource partagée, avec le même groupe homologue disponible pour plusieurs applications. si plusieurs applications pour la même identité et Windows utilisateur utilisent le même groupe pair, elles partagent également la même base de données sous-jacente et les mêmes connexions (voisin et direct). Si l’une de ces applications appelle [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), toutes les autres applications pour cette identité/cet utilisateur participant au groupe se connectent également au groupe. Si un enregistrement est ajouté par une application alors que le groupe est hors connexion, d’autres applications sont également en mesure de le voir. En conséquence, une application doit être prête à se connecter à tout moment.

## <a name="connecting-to-a-peer-group-online"></a>Connexion à un groupe homologue (en ligne)

Pour commencer à participer à un groupe, appelez [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) après avoir créé, rejoint ou ouvert le groupe. Dans cet État, les connexions directes peuvent être ouvertes avec d’autres pairs qui participent au même groupe en appelant [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Pour détecter si une tentative de connexion a échoué, inscrivez-vous à l' \_ événement d’échec de connexion d’événement de groupe pair \_ \_ \_ . Cet événement est déclenché si l’infrastructure de regroupement ne peut pas trouver un autre membre auquel se connecter, ou si la connexion échoue avant la synchronisation de la base de données de groupe et qu’une autre connexion ne peut pas être établie.

Bien que plusieurs applications qui s’exécutent sur l’homologue et qui participent au même groupe avec la même identité d’homologue puissent être hors connexion, un appel à [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) par l’une des applications entraîne la mise en ligne de toutes les applications.

En outre, si une application sur l’homologue s’est connectée au groupe, toutes les autres applications qui appellent [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) sont immédiatement connectées. Si une application appelle [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), le descripteur est fermé uniquement pour cette application. Par conséquent, un appel ultérieur à **PeerGroupOpen** par l’application retourne un nouveau descripteur de groupe et l’application est mise en ligne immédiatement si d’autres applications qui participent au même groupe sont toujours connectées.

## <a name="sending-and-receiving-data"></a>Envoi et réception de données

Pour envoyer et recevoir des données entre des nœuds membres spécifiques du groupe, les connexions directes doivent être établies avec les membres avec lesquels vous souhaitez interagir. L’établissement d’une connexion directe est un appel asynchrone à [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), en passant le handle d’un groupe connecté, ainsi que l’identité de l’homologue dans le groupe auquel vous souhaitez vous connecter. Cette méthode renverra un ID de connexion. Si l’appel réussit, un \_ événement de \_ \_ connexion directe d’événement de groupe pair \_ est déclenché sur l’homologue, en validant l’ID de connexion.

Pour recevoir des connexions directes d’autres homologues en ligne, inscrivez-vous à l' \_ événement de connexion directe d’événement de groupe homologue \_ \_ \_ avec un appel à [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Une fois qu’une connexion directe a été établie, l’application peut commencer à envoyer des données avec des appels à [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata), en transmettant l’ID de connexion valide. L’ordonnancement des transmissions de données à parties multiples est géré par **PeerGroupSendData**. Toutefois, les applications doivent implémenter une pile de protocole appropriée pour gérer les données opaques retournées par cet appel d’API.

Pour recevoir des données via une connexion directe, l’application doit s’inscrire à \_ l' \_ événement de données entrantes de l’événement de groupe pair \_ \_ avec [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). Le gestionnaire d’événements est chargé d’obtenir et de classer les données opaques et de les transmettre à l’application. Ces données sont obtenues dans le gestionnaire d’événements en appelant [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) avec le descripteur des événements inscrits.

Une connexion directe est fermée en appelant [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) et en passant l’ID de connexion obtenu lors d’un appel précédent à [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) ou reçu dans les données d’événement pour la \_ \_ connexion directe au groupe d’événements homologues \_ \_ .

 

 



