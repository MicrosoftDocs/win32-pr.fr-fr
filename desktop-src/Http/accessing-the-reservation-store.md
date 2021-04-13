---
title: Accès au magasin de réservations
description: L’API du serveur HTTP conserve la liste de réservation d’espace de noms pour tous les utilisateurs sur l’ordinateur.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Accès au magasin de réservations HTTP
- Magasin de réservation HTTP, accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379954"
---
# <a name="accessing-the-reservation-store"></a>Accès au magasin de réservations

L’API du serveur HTTP conserve la liste de réservation d’espace de noms pour tous les utilisateurs sur l’ordinateur. Une entrée de réservation se compose d’un [URLPrefix](urlprefix-strings.md) et d’une liste de contrôle d’accès correspondante. Chaque UrlPrefix dans le magasin a une liste de contrôle d’accès qui répertorie tous les utilisateurs qui sont autorisés à s’inscrire pour recevoir des demandes pour l’espace de noms. Les utilisateurs disposant de privilèges de délégation peuvent déléguer des sous-arborescences de l’espace de noms dont ils sont propriétaires à d’autres utilisateurs ou supprimer des réservations existantes à l’aide des API de configuration.

Pour ajouter une réservation au magasin de réservation persistante, l’application appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre ID de configuration défini sur la valeur **HttpServiceConfigUrlAclInfo** . L’API du serveur HTTP vérifie la propriété de l’espace de noms et l’ID de l’utilisateur avant d’ajouter une réservation au magasin.

L’API du serveur HTTP fournit également des fonctions pour interroger et supprimer les configurations de service pour les espaces de noms d’URL. La fonction [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) appelée avec le paramètre ID de configuration défini sur les requêtes de valeur **HttpServiceConfigUrlAclInfo** et la fonction [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) supprime sur le magasin d’espaces de noms d’URL.

 

 




