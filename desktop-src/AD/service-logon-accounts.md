---
title: Comptes d’ouverture de session du service
description: Un service, comme n’importe quel processus, a une identité de sécurité principale qui détermine les droits d’accès et les privilèges accordés pour les ressources locales et réseau.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, ouverture de session du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839266"
---
# <a name="service-logon-accounts"></a>Comptes d’ouverture de session du service

Un service, comme n’importe quel processus, a une identité de sécurité principale qui détermine les droits d’accès et les privilèges accordés pour les ressources locales et réseau. Cette identité de sécurité, ou contexte de sécurité, détermine également le potentiel du service pour endommager les ressources locales et réseau.

Le contexte de sécurité d’un service Microsoft Win32 est déterminé par le compte d’ouverture de session utilisé pour démarrer le service. Cette section traite des problèmes de programmation et des meilleures pratiques en rapport avec le compte d’ouverture de session du service utilisé par les services Win32, en se concentrant sur les services Active Directory. Cette section comprend les rubriques suivantes :

-   [À propos des comptes d’ouverture de session du service](about-service-logon-accounts.md): présentation des comptes d’ouverture de session du service et des problèmes de programmation du contexte de sécurité pour un service Win32.
-   [Instructions pour la sélection d’un compte d’ouverture de session de service](guidelines-for-selecting-a-service-logon-account.md) pour un service Win32.
-   [Configuration du compte d’utilisateur d’un service](setting-up-a-serviceampaposs-user-account.md).
-   [Installation d’un service sur un ordinateur hôte](installing-a-service-on-a-host-computer.md) et spécification du compte d’ouverture de session du service.
-   [Octroi de l’ouverture de session en tant que service sur l’ordinateur hôte](granting-logon-as-service-right-on-the-host-computer.md): octroi au compte d’utilisateur du service le droit ouvrir une session en tant que service sur l’ordinateur hôte.
-   [Test de l’exécution sur un contrôleur de domaine](testing-whether-running-on-a-domain-controller.md)— la détection au moment de l’installation si l’instance de service est en cours d’installation sur un contrôleur de domaine.
-   [Octroi de droits d’accès au compte d’ouverture de session du service](granting-access-rights-to-the-service-logon-account.md): la définition et la gestion des ACE et des appartenances aux groupes permettent de s’assurer que le système accorde l’accès au service en cours aux ressources locales et réseau nécessaires.
-   [Modification du mot de passe sur le compte d’utilisateur d’un service](changing-the-password-on-a-serviceampaposs-user-account.md): modification du mot de passe sur le compte d’utilisateur d’un service et mise à jour en même temps du mot de passe inscrit auprès du gestionnaire de contrôle des services sur chaque serveur hôte sur lequel le service est installé.
-   [Authentification mutuelle à l’aide de Kerberos](mutual-authentication-using-kerberos.md): conservation de l’inscription du nom de principal du service (SPN) sur l’objet d’annuaire associé au compte d’ouverture de session de chaque instance de votre service. Les SPN permettent aux clients d’authentifier un service à l’aide de l’authentification mutuelle Kerberos.
-   [Conversion des formats de nom de compte de domaine](converting-domain-account-name-formats.md)(par exemple, conversion d’un nom unique au format de nom ****\\*** d’utilisateur de domaine* , et vice versa).

 

 




