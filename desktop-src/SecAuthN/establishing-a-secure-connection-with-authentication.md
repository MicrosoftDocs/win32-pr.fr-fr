---
description: Dans un protocole d’application client/serveur, un serveur est lié à un port de communication, tel qu’un socket ou une interface RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Établissement d’une connexion sécurisée avec authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5f9458cf578481e049dcf2b41d6607b3c6151ce16a938cfe0e398ae7b3bf56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008247"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Établissement d’une connexion sécurisée avec authentification

Dans un [*protocole d’application*](/windows/desktop/SecGloss/a-gly)client/serveur, un serveur est lié à un port de communication, tel qu’un socket ou une interface RPC. Le serveur attend ensuite qu’un client se connecte et demande le service. Le rôle de sécurité au niveau de la configuration de la connexion est bidirectionnel dans le cas de l’authentification mutuelle :

-   Authentification du client par le serveur.
-   Authentification du serveur par le client.

Les composants client et serveur d’une application de transport utilisent un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour établir une connexion sécurisée pour la transmission des messages. La première étape de l’établissement d’une connexion sécurisée consiste à créer un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly). autrement dit, une structure de données opaque qui contient les données de sécurité relatives à une connexion, telles qu’une [*clé de session*](/windows/desktop/SecGloss/s-gly) et la durée de la session.

Un contexte de sécurité est essentiellement un message du package de sécurité associé au client au package de sécurité associé au serveur. Par conséquent, la création d’un contexte de sécurité nécessite généralement que le client et le serveur effectuent des appels à leurs packages de sécurité respectifs. Pour plus d’informations sur les fonctions de contexte, consultez [gestion du contexte](authentication-functions.md).

Le protocole utilisé pour établir une connexion authentifiée sécurisée implique l’échange d’un ou plusieurs « jetons de sécurité » entre le client et le serveur. Ces jetons sont envoyés en tant que messages opaques par les deux côtés, ainsi que toutes les autres informations spécifiques au [*protocole d’application*](/windows/desktop/SecGloss/a-gly). En tant que message opaque, le jeton est reçu d’une fonction de package de sécurité par le client, qui ne peut pas l’interpréter ou le modifier, et est transféré en tant que message au serveur. Le jeton est également opaque sur le serveur, qui ne peut ni interpréter, ni modifier le jeton. Le serveur transfère le jeton opaque à son package de sécurité pour interprétation. Le package informe ensuite le serveur de l’authentification du client ou de l’échec de l’authentification.

Le client reçoit le jeton du serveur dans un message, récupère le jeton à partir du message reçu et utilise ce jeton dans un appel à son package de sécurité. Le client appelle à nouveau le package de sécurité, indiquant si une connexion sécurisée a été établie ou si des échanges supplémentaires sont nécessaires avant la préparation d’une connexion sécurisée. En théorie, il n’existe aucune limite quant au nombre d’échanges de jetons de sécurité nécessaires. Dans la pratique, seul un nombre limité d’échanges est requis. L’authentification NTLM est basée sur le schéma de stimulation/réponse et utilise trois jambes pour authentifier un client auprès du serveur. Le protocole [*Kerberos*](/windows/desktop/SecGloss/k-gly) version 5,0 peut nécessiter des échanges de messages supplémentaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Initialisation du contexte client](client-context-initialization.md)
</dt> <dt>

[Initialisation du contexte de serveur](server-context-initialization.md)
</dt> </dl>

 

 
