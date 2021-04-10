---
title: Rappels (RPC)
description: Souvent, le modèle de programmation requiert un rappel de serveur pour un client via un appel de procédure distante (RPC) ou des appels clients vers un serveur non approuvé. Cela introduit de nombreux pièges potentiels.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032265"
---
# <a name="callbacks-rpc"></a>Rappels (RPC)

Souvent, le modèle de programmation requiert un rappel de serveur pour un client via un appel de procédure distante (RPC) ou des appels clients vers un serveur non approuvé. Cela introduit de nombreux pièges potentiels.

Tout d’abord, le rappel au client doit être effectué avec un niveau d’emprunt d’identité suffisamment faible. Si le serveur est un service système hautement privilégié, le fait de rappeler un client local avec un niveau d’emprunt d’identité d’emprunt d’identité ou supérieur peut fournir au client des privilèges suffisants pour prendre le contrôle du système. Le fait de rappeler un client distant avec un niveau d’emprunt d’identité plus élevé que nécessaire peut également entraîner des conséquences indésirables.

Deuxièmement, si une personne malveillante induit votre service pour effectuer un rappel, elle peut *lancer une attaque* par déni de service. Ces attaques ne sont pas spécifiques à RPC. dans ces attaques, une machine vous induit de lui envoyer du trafic, mais elle ne répond pas à vos demandes. Vous pouvez recevoir plus et plus de ressources pour appeler le trou noir, mais ils ne sont jamais refondus. Une attaque au niveau du TCP appelée attaque de flux SYN TCP/IP est un exemple générique d’une telle attaque.

Au niveau RPC, une attaque de trou noir simple se produit lorsqu’un pirate appelle une interface et demande au serveur d’appeler l’interface. L’interface est conforme, mais l’attaquant ne retourne jamais l’appel : un thread sur le serveur est lié. L’attaquant effectue cette 100 fois, en liant 100 threads sur le serveur. Le serveur finit par manquer de mémoire. Le débogage du serveur peut révéler potentiellement l’identité de l’appelant de trou noir, mais souvent, le serveur est redémarré sans soupçonner la présence d’un élément indésirable, ou il n’y a pas suffisamment d’expertise disponible pour déterminer l’attaquant.

Le troisième piège se trouve sur le client. Souvent, un client effectue un appel au serveur informant le serveur de la façon de le rappeler (généralement une liaison de chaîne), puis attend qu’un appel du serveur arrive, en acceptant en aveugle les appels sur ce point de terminaison qui affirment provenir du serveur. Le protocole de rappel du serveur vers le client doit inclure un mécanisme de vérification pour s’assurer que, lorsque le rappel vient au client, il provient en fait du serveur.

 

 




