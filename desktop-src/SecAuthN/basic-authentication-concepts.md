---
description: Dans un modèle d’application client/serveur, les clients sont des programmes agissant pour le compte des utilisateurs qui ont besoin d’une opération.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Concepts d’authentification de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416563"
---
# <a name="basic-authentication-concepts"></a>Concepts d’authentification de base

Dans un modèle d’application client/serveur, les clients sont des programmes agissant pour le compte des utilisateurs qui ont besoin d’une opération. Cela peut consister à ouvrir et à utiliser un fichier, à accéder à une boîte aux lettres, à interroger une base de données ou à imprimer un document. Les serveurs sont des programmes qui fournissent des services aux clients, tels que le stockage de fichiers, la gestion des messages, le traitement des requêtes et la mise en attente d’impression. Actions initiées par les clients, les serveurs répondent. En règle générale, un serveur est à l’écoute d’un port de communication en attente de la connexion des clients et de la demande de service.

Dans le modèle de protocole Kerberos, chaque connexion client/serveur commence par l'authentification. L'un après l'autre, le client et le serveur passent par une séquence d'actions visant à vérifier l'authenticité de la partie située à l'extrémité opposée de la connexion. Si l'authentification réussit, la configuration de la session est effectuée et une session client/serveur sécurisée est établie.

Le protocole Kerberos utilise les éléments suivants :

-   [Authentification par clé](key-authentication.md)
-   [messages Authenticator](authenticator-messages.md)
-   [Distribution de clés](key-distribution.md)
-   [Tickets de session](session-tickets.md)
-   [Tickets d’accord de tickets](ticket-granting-tickets.md)

 

 



