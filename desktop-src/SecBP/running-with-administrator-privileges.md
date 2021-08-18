---
description: Pour éviter les attaques malveillantes, déterminez si votre application requiert des privilèges d’administrateur. pour les fonctions qui nécessitent des autorisations d’administrateur, créez une application distincte et utilisez la commande de ligne de commande Windows RunAs.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Exécution avec des privilèges d’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622719"
---
# <a name="running-with-administrator-privileges"></a>Exécution avec des privilèges d’administrateur

La première étape pour déterminer le type de compte que votre application doit exécuter consiste à examiner les ressources que l’application utilisera et les API privilégiées qu’elle appellera. Vous constaterez peut-être que l’application, ou ses grandes parties, ne nécessitent pas de privilèges d’administrateur. L' *écriture de code sécurisé*, par Michael Howard et David LeBlanc, offre une excellente description de la façon d’effectuer cette évaluation et est fortement recommandée. (Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)

Vous pouvez fournir les privilèges dont votre application a besoin pour réduire les risques d’attaques malveillantes en utilisant l’une des approches suivantes :

-   Exécutez sous un compte avec moins de privilèges. Pour ce faire, vous pouvez utiliser [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) pour déterminer les privilèges qui sont activés dans un jeton. Si les privilèges disponibles ne sont pas adaptés à l’opération en cours, vous pouvez désactiver ce code et demander à l’utilisateur de se connecter à un compte disposant de privilèges d’administrateur.
-   S’arrêter dans des fonctions d’application distinctes qui nécessitent des autorisations d’administrateur. Vous pouvez fournir à l’utilisateur un raccourci qui exécute la commande RunAs. Pour obtenir des instructions détaillées sur la façon de configurer le raccourci, recherchez « runas » dans l’aide. Par programme, vous pouvez configurer la commande [runas](/windows/desktop/com/runas) sous la clé de registre de la [clé AppID](/windows/desktop/com/appid-key) pour votre application.
-   Authentifiez l’utilisateur en appelant [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) ou [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (ligne de commande) pour obtenir le nom d’utilisateur et le mot de passe. Pour obtenir un exemple, consultez [demande d’informations d’identification à l’utilisateur](asking-the-user-for-credentials.md).
-   Emprunter l’identité de l’utilisateur. Un processus qui démarre sous un compte à privilèges élevés comme System peut emprunter l’identité d’un compte d’utilisateur en appelant [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) ou des fonctions d’emprunt d’identité similaires, réduisant ainsi le niveau de privilège. Toutefois, si un appel à [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) est injecté dans le thread, le processus revient aux privilèges système d’origine.

Si vous avez déterminé que votre application doit s’exécuter sous un compte disposant de privilèges d’administrateur et qu’un mot de passe d’administrateur doit être stocké dans le système logiciel, consultez [gestion des mots de passe](handling-passwords.md) pour les méthodes de ce faire en toute sécurité.

 

 
