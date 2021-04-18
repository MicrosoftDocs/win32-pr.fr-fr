---
description: Au lieu d’envoyer les clés de session chiffrées aux deux principaux, le KDC envoie les copies du client et du serveur de la clé de session au client.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Tickets de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519882"
---
# <a name="session-tickets"></a>Tickets de session

Au lieu d’envoyer les clés de session chiffrées aux deux principaux, le [KDC](key-distribution-center.md) envoie les copies du client et du serveur de la [*clé de session*](../secgloss/s-gly.md) au client. La copie du client de la clé de session est chiffrée avec la [*clé principale*](../secgloss/m-gly.md) du client et ne peut donc pas être déchiffrée par une autre entité. La copie du serveur de la clé de session est incorporée, ainsi que les données d’autorisation relatives au client, dans une structure de données appelée ticket. Le ticket est entièrement chiffré avec la clé principale du serveur et, par conséquent, il ne peut pas être lu ou modifié par le client ou toute autre entité qui n’a pas accès à la clé principale du serveur. Il incombe au client de stocker le ticket en toute sécurité jusqu’à ce qu’il contacte le serveur.

> [!Note]  
> Le centre de distribution de clés fournit uniquement un service d’accord de tickets. Le client et le serveur sont responsables du maintien de la sécurité de leurs clés principales respectives.

 

Lorsque le client reçoit la réponse du KDC, il extrait le ticket et sa propre copie de la clé de session, en les plaçant dans un cache sécurisé. Pour établir une session sécurisée avec le serveur, il envoie au serveur un message contenant le ticket, toujours chiffré avec la clé principale du serveur et un message d' [authentificateur](authenticator-messages.md) chiffré avec la clé de session. Ensemble, le ticket et le message de l’authentificateur sont les [*informations d’identification*](../secgloss/c-gly.md) du client pour le serveur.

Lorsque le serveur reçoit les informations d’identification d’un client, il déchiffre le ticket avec sa [*clé principale*](../secgloss/m-gly.md), extrait la [*clé de session*](../secgloss/s-gly.md)et utilise la clé de session pour déchiffrer le message de l’authentificateur du client. Si tout est vérifié, le serveur sait que les informations d’identification du client ont été émises par le KDC, une autorité approuvée. Pour l’authentification mutuelle, le serveur répond en chiffrant l’horodatage à partir du message de l’authentificateur du client à l’aide de la clé de session. Ce message chiffré est envoyé au client. Le client déchiffre ensuite le message. Si le message retourné est le même que l’horodatage dans le message de l’authentificateur d’origine, le serveur est authentifié.

En guise d’avantage supplémentaire, le serveur n’a pas besoin de stocker les clés de session qu’il utilise avec ses clients. Chaque client est chargé de gérer le ticket pour le serveur dans son cache de tickets et de présenter ce ticket chaque fois qu’il accède au serveur. Chaque fois que le serveur reçoit un ticket d’un client, il utilise sa clé principale pour déchiffrer le ticket et extraire la clé de session. Lorsque le serveur n’a plus besoin de la clé de session, la clé est supprimée.

Le client n’a pas besoin d’accéder au centre de données à chaque fois qu’il souhaite accéder à ce serveur. Les tickets peuvent être réutilisés. En guise de précaution contre le risque de vol de tickets, les tickets ont un délai d’expiration spécifié par le KDC dans la structure de ticket. La durée de validité d’un ticket dépend de la stratégie Kerberos pour le domaine. En règle générale, les tickets sont valables pendant plus de huit heures, à savoir la durée d’une [*session de connexion*](../secgloss/l-gly.md)normale. Lorsque l’utilisateur d’une station de travail cliente se déconnecte, le cache du ticket client est vidé et tous les tickets et les clés de session client sont détruits.

 

 
