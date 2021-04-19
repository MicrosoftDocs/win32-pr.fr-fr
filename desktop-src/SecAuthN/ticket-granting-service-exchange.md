---
description: Une fois qu’un ticket TGT (Ticket-Granting Ticket) et une clé de session ont été établis pour le client, le client peut demander une clé de session et un ticket distincts pour le service.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Échange de service TG (ticket-granting)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529758"
---
# <a name="ticket-granting-service-exchange"></a>Échange de service TG (ticket-granting)

Une fois qu’un ticket TGT (Ticket-Granting Ticket) et une [*clé de session*](../secgloss/s-gly.md) ont été établis pour le client, le client peut demander une clé de session et un ticket distincts pour le service.

**Pour demander un ticket pour un autre service**

1.  Le client Kerberos sur la station de travail de l’utilisateur demande des [*informations d’identification*](../secgloss/c-gly.md) pour le service en envoyant au [*Centre de distribution de clés*](../secgloss/k-gly.md) (KDC) un message de type KRB \_ TGS \_ REQ (demande de service de Ticket-Granting Kerberos). Ce message est constitué de l’identité du service pour lequel le client demande des informations d’identification, d’un message d’authentificateur chiffré avec la nouvelle [*clé de session*](../secgloss/s-gly.md)de connexion de l’utilisateur et du TGT obtenu auprès de l' [échange du service d’authentification](authentication-service-exchange.md).
2.  Lorsque le KDC reçoit une \_ demande TGS de KRB \_ , le KDC déchiffre le ticket TGT avec sa clé secrète et extrait la clé de session de connexion de l’utilisateur.
3.  Le KDC utilise la [*clé de session*](../secgloss/s-gly.md) de connexion pour déchiffrer le message de l’authentificateur de l’utilisateur et l’évalue. Si l’authentificateur réussit le test, le KDC extrait les données d’autorisation de l’utilisateur à partir du TGT et invente une clé de session à partager avec le serveur demandé.
4.  Le KDC chiffre une copie de la clé de session de service avec la clé de session de connexion de l’utilisateur.
5.  Le KDC incorpore une autre copie de la clé de session de service dans un ticket, avec les données d’autorisation de l’utilisateur, et chiffre le ticket avec la [*clé principale*](../secgloss/m-gly.md)du serveur.
6.  Le KDC renvoie ces informations d’identification au client en répondant à l’aide d’un message de type KRB \_ TGS \_ Rep (Kerberos Ticket-Granting service Reply).
7.  Lorsque le client reçoit la réponse, il déchiffre la clé de session de service avec la clé de session de connexion de l’utilisateur et stocke la clé de session de service dans son cache de tickets.
8.  Le client extrait le ticket sur le serveur et le stocke dans son cache de tickets.

 

 
