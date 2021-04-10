---
title: À propos des comptes d’ouverture de session de service
description: Lorsqu’un service Win32 démarre, il ouvre une session sur l’ordinateur local.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328b33d5dab36ccc5a803eb7c43ca3112e96ecf8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101404"
---
# <a name="about-service-logon-accounts"></a>À propos des comptes d’ouverture de session de service

Lorsqu’un service Win32 démarre, il ouvre une session sur l’ordinateur local. Il peut ouvrir une session en tant que :

-   Un compte d’utilisateur local ou de domaine.
-   Compte LocalSystem.

Le compte d’ouverture de session détermine l’identité de sécurité du service au moment de l’exécution, autrement dit, le contexte de sécurité principal du service. Le contexte de sécurité détermine la capacité du service à accéder aux ressources locales et réseau. Par exemple, un service qui s’exécute dans le contexte de sécurité d’un compte d’utilisateur local ne peut pas accéder aux ressources réseau. À l’inverse, un service s’exécutant dans le contexte de sécurité du compte LocalSystem sur un contrôleur de domaine Windows 2000 (DC) dispose d’un accès illimité au contrôleur de domaine. Pour plus d’informations et pour obtenir une description des avantages et des limitations entre les comptes d’utilisateur et LocalSystem, consultez [contextes de sécurité et Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

Enfin, les administrateurs sur le système où le service est installé ont le contrôle sur le compte d’ouverture de session du service. Pour des raisons de sécurité, certains administrateurs peuvent ne pas vous autoriser à installer votre service sous le compte LocalSystem. Votre service doit pouvoir s’exécuter sous un compte d’utilisateur de domaine. En tant que programmeur, vous pouvez exercer un contrôle sur le compte d’ouverture de session de votre service. Votre programme d’installation de service spécifie le compte d’ouverture de session du service lorsqu’il appelle la fonction [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) pour installer le service sur un ordinateur hôte. Votre programme d’installation peut suggérer un compte d’ouverture de session par défaut, mais il doit autoriser un administrateur à spécifier le compte réel.

Votre programme d’installation peut également effectuer les tâches suivantes relatives au compte d’ouverture de session de votre service :

-   Installation. Si vous installez votre service pour qu’il s’exécute sous un compte d’utilisateur, le compte doit exister avant d’appeler [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Vous pouvez utiliser un compte existant ou en créer un dans le cadre de l’installrt de l’ordinateur hôte. Pour plus d’informations, consultez [configuration d’un compte d’utilisateur de service](setting-up-a-serviceampaposs-user-account.md).
-   Authentification. Si vous souhaitez que les clients utilisent l’authentification mutuelle Kerberos, inscrivez les noms de principal du service sur le compte d’ouverture de session du service. Si le service s’exécute sous le compte LocalSystem, le compte d’ouverture de session du service est le compte d’ordinateur de l’ordinateur hôte. Pour plus d'informations, consultez la page [Noms de principal de service](service-principal-names.md).
-   Accorder l’accès. Assurez-vous que le service au moment de l’exécution dispose des droits d’accès et des privilèges nécessaires pour effectuer ses tâches. Cela peut nécessiter la définition des entrées de contrôle d’accès (ACE) dans les descripteurs de sécurité de diverses ressources, c’est-à-dire des objets d’annuaire, des partages de fichiers, etc., afin d’accorder les droits d’accès nécessaires au compte d’utilisateur ou d’ordinateur. Pour plus d’informations, consultez [octroi de droits d’accès au compte d’ouverture de session du service](granting-access-rights-to-the-service-logon-account.md).
-   Définir des privilèges. Affectez des privilèges au compte d’ouverture de session spécifié, par exemple le droit d’ouvrir une session en tant que service sur l’ordinateur hôte. Pour plus d’informations, consultez [accorder des droits d’ouverture de session en tant que service sur l’ordinateur hôte](granting-logon-as-service-right-on-the-host-computer.md).

Après l’installation d’un service, des tâches de maintenance sont liées à votre compte d’ouverture de session du service. Pour plus d’informations, consultez [tâches de maintenance de compte d’ouverture de session](logon-account-maintenance-tasks.md).

-   Maintenance des mots de passe. Pour un service qui s’exécute sous un compte d’utilisateur, vous devez modifier régulièrement le mot de passe et conserver le mot de passe synchronisé avec le mot de passe utilisé par un ou plusieurs gestionnaires de contrôle des services locaux pour démarrer le service.
-   Maintenance du SPN. Si un compte d’ouverture de session de service change, supprimez les SPN inscrits sur l’ancien compte et inscrivez-les sur le nouveau compte. Sachez que lorsqu’un service est installé, un administrateur de domaine peut modifier le compte sous lequel votre service s’exécute ; Utilisez les fonctions Win32 ou l’interface utilisateur de l’outil d’administration gestion de l’ordinateur.
-   Maintenance ACE. Si un compte d’ouverture de session de service change, vous devez mettre à jour les ACE et les appartenances aux groupes pour vous assurer que le service peut toujours accéder aux ressources nécessaires.

 

 