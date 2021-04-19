---
description: L’utilisateur commence à ouvrir une session sur le réseau en tapant un nom d’ouverture de session et un mot de passe. Le client Kerberos sur la station de travail de l’utilisateur convertit le mot de passe en une clé de chiffrement et enregistre le résultat dans une variable de programme.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Échange de service d'authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14121ed33ae0ac169c590b03dfb0b395306d11f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544927"
---
# <a name="authentication-service-exchange"></a>Échange de service d'authentification

L’utilisateur commence à ouvrir une session sur le réseau en tapant un nom d’ouverture de session et un mot de passe. Le client [*Kerberos*](/windows/desktop/SecGloss/k-gly) sur la station de travail de l’utilisateur convertit le mot de passe en une clé de chiffrement et enregistre le résultat dans une variable de programme.

Le client demande ensuite des [*informations d’identification*](/windows/desktop/SecGloss/c-gly) pour le TGS (Ticket-Granting Service) du [*Centre de distribution de clés*](/windows/desktop/SecGloss/k-gly) (KDC) en envoyant au service d’authentification du KDC un message de type KRB \_ comme \_ req (demande de service d’authentification Kerberos). La première partie de ce message identifie l’utilisateur et le service TGS demandé. La deuxième partie de ce message contient des données de pré-authentification destinées à prouver que l’utilisateur connaît le mot de passe. Il s’agit simplement d’un message d’authentificateur chiffré avec la [*clé principale*](/windows/desktop/SecGloss/m-gly) dérivée du mot de passe d’ouverture de session de l’utilisateur.

Lorsque le KDC reçoit le KRB \_ comme \_ req, il recherche l’utilisateur dans sa base de données, obtient la clé principale de l’utilisateur associé, déchiffre les données de pré-authentification et évalue l’horodatage à l’intérieur de. Si l’horodatage est valide, le KDC peut être certain que les données de pré-authentification ont été chiffrées à l’aide de la clé principale de l’utilisateur et que le client est donc authentique.

Une fois que le KDC a vérifié l’identité de l’utilisateur, il crée des informations d’identification que le client peut présenter au TGS, comme suit :

1.  Le KDC invente une clé de [*session*](/windows/desktop/SecGloss/s-gly) de connexion et chiffre une copie avec la clé principale de l’utilisateur.
2.  Le centre de distribution de clés incorpore une autre copie de la clé de session de connexion et les données d’autorisation de l’utilisateur dans un ticket TGT (Ticket-Granting Ticket) et chiffre le ticket TGT avec la propre clé principale du KDC.
3.  Le KDC renvoie ces informations d’identification au client en répondant avec un message de type KRB \_ As \_ Rep (Kerberos Authentication Service Reply).
4.  Lorsque le client reçoit la réponse, il utilise la clé dérivée du mot de passe de l’utilisateur pour déchiffrer la nouvelle clé de session de connexion.
5.  Le client stocke la nouvelle clé dans son cache de tickets.
6.  Le client extrait le ticket TGT du message et le stocke également dans son cache de tickets.

 

 
