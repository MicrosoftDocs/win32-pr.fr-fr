---
description: Explique les deux types d’informations d’identification avec lesquelles l’API de gestion des informations d’identification fonctionne.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Types d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d0e067b3918496310f3244153864abbf7548e5367569f4f2fbd06de40f207c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140932"
---
# <a name="kinds-of-credentials"></a>Types d’informations d’identification

L’API de gestion des informations d’identification fonctionne avec deux types d’informations d’identification :

-   [Informations d’identification de domaine](#domain-credentials)
-   [Informations d’identification génériques](#generic-credentials)

## <a name="domain-credentials"></a>Informations d'identification du domaine

Les informations d’identification de domaine sont utilisées par le système d’exploitation et sont authentifiées par l’autorité de sécurité locale (LSA). En règle générale, les informations d’identification de domaine sont établies pour un utilisateur lorsqu’un package de sécurité enregistré, tel que le protocole Kerberos, authentifie les données de connexion fournies par l’utilisateur. Les informations d’identification de connexion sont mises en cache par le système d’exploitation afin qu’une authentification unique donne à l’utilisateur l’accès à de nombreuses ressources différentes. Par exemple, les connexions réseau peuvent se produire de manière transparente et l’accès aux objets système protégés peut être accordé en fonction des informations d’identification de domaine mises en cache de l’utilisateur.

Les fonctions de gestion des informations d’identification fournissent un mécanisme permettant aux applications d’inviter un utilisateur à entrer des informations d’identification de domaine une fois que l’utilisateur ouvre une session et de demander au système d’exploitation d’authentifier les informations fournies par l’utilisateur.

La partie secrète des informations d’identification de domaine, le mot de passe, est protégée par le système d’exploitation. Seul le code qui s’exécute in-process avec l’autorité LSA peut lire et écrire des informations d’identification de domaine. Les applications sont limitées à l’écriture des informations d’identification de domaine.

Windows prend en charge l’utilisation développée des informations d’identification de carte à puce et de certificat. Pour garantir la sécurité, l’API de gestion des informations d’identification ne stocke jamais le code confidentiel de la carte à puce sur l’ordinateur.

## <a name="generic-credentials"></a>Informations d’identification génériques

Les informations d’identification génériques sont définies et authentifiées par des applications qui gèrent l’autorisation et la sécurité directement au lieu de déléguer ces tâches au système d’exploitation. Par exemple, une application peut demander aux utilisateurs d’entrer un nom d’utilisateur et un mot de passe fournis par l’application ou de générer un [*certificat*](../secgloss/c-gly.md) pour accéder à un site Web.

Les applications utilisent des fonctions de gestion des informations d’identification pour inviter les utilisateurs à fournir des informations d’identification définies par l’application, génériques, telles que le nom d’utilisateur, le certificat, la carte à puce ou le mot de passe. Les informations entrées par l’utilisateur sont retournées à l’application pour l’authentification.

La gestion des informations d’identification fournit une gestion du cache personnalisable et un stockage à long terme pour les informations d’identification génériques. Les informations d’identification génériques peuvent être lues et écrites par les processus utilisateur.

 

 
