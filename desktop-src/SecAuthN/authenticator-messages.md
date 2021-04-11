---
description: Dans un protocole simple utilisant l’authentification par clé secrète, un client présente un message d’authentificateur sous la forme d’une information chiffrée dans la clé de session.
ms.assetid: 984c84db-96d5-479e-8917-25a0270b3b59
title: Messages de l’authentificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e76cf171d163ac2f1d0d4a7fcaab53a7fa0ace0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203378"
---
# <a name="authenticator-messages"></a>Messages de l’authentificateur

Dans un protocole simple utilisant l’authentification par clé secrète, un client présente un message d’authentificateur sous la forme d’une information chiffrée dans la [*clé de session*](/windows/desktop/SecGloss/s-gly). Les informations contenues dans le message de l’authentificateur doivent être différentes chaque fois que le protocole d’authentification est exécuté, ou un message d’authentificateur chiffré peut être réutilisé par une entité non autorisée.

Lors de la réception du message de l’authentificateur, le serveur le déchiffre et peut déterminer à partir du contenu du message déchiffré si le déchiffrement a réussi. Si le message déchiffré n’est pas incompréhensible, le serveur sait que le client qui présente le message de l’authentificateur a utilisé la clé correcte pour chiffrer le message. Seules deux entités ont accès à la [*clé de session*](/windows/desktop/SecGloss/s-gly) et si le serveur est l’un de ceux-ci, le client qui a chiffré le message de l’authentificateur doit être l’autre.

Pour l’authentification mutuelle, un protocole similaire est exécuté. Le serveur extrait une partie des informations du message d’authentificateur d’origine déchiffré, le chiffre avec la clé de session partagée et envoie le message chiffré au client. Le client déchiffre le message et compare le résultat avec le d’origine. Si le message déchiffré correspond à la partie correcte du message d’origine, le client sait que le serveur a pu déchiffrer le message d’origine avec la clé de session de secret partagé et a pu rechiffrer une partie de ce message avec cette même [*clé de session*](/windows/desktop/SecGloss/s-gly)secrète partagée.

 

 
