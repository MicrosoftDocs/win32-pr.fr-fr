---
description: Chaque service s’exécute dans le contexte de sécurité d’un compte d’utilisateur.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Comptes d’utilisateur de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868178"
---
# <a name="service-user-accounts"></a>Comptes d’utilisateur de service

Chaque service s’exécute dans le contexte de sécurité d’un compte d’utilisateur. Le nom d’utilisateur et le mot de passe d’un compte sont spécifiés par la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) au moment de l’installation du service. Le nom d’utilisateur et le mot de passe peuvent être modifiés à l’aide de la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Vous pouvez utiliser la fonction [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) pour obtenir le nom d’utilisateur (mais pas le mot de passe) associé à un objet de service. Le gestionnaire de contrôle des services (SCM) charge automatiquement le profil utilisateur.

Lors du démarrage d’un service, le SCM se connecte au compte associé au service. Si la connexion réussit, le système génère un jeton d’accès et l’attache au nouveau processus de service. Ce jeton identifie le processus de service dans toutes les interactions suivantes avec des objets sécurisables (objets auxquels est associé un descripteur de sécurité). Par exemple, si le service tente d’ouvrir un handle vers un canal, le système compare le jeton d’accès du service au descripteur de sécurité du canal avant d’accorder l’accès.

Le SCM ne conserve pas les mots de passe des comptes d’utilisateur de service. Si un mot de passe a expiré, l’ouverture de session échoue et le service ne peut pas démarrer. L’administrateur système qui attribue des comptes aux services peut créer des comptes avec des mots de passe qui n’expirent jamais. L’administrateur peut également gérer les comptes dont les mots de passe expirent à l’aide d’un [programme de configuration de service](service-configuration-programs.md) pour modifier régulièrement les mots de passe.

Si un service doit reconnaître un autre service avant de partager ses informations, le deuxième service peut utiliser le même compte que le premier service, ou il peut s’exécuter dans un compte appartenant à un alias qui est reconnu par le premier service. Les services qui doivent s’exécuter de façon distribuée sur le réseau doivent s’exécuter dans des comptes à l’échelle du domaine.

Vous pouvez spécifier l’un des comptes spéciaux suivants au lieu de spécifier un compte d’utilisateur pour le service :

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



