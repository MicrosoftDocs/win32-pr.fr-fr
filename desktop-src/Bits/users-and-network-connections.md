---
title: Utilisateurs et connexions réseau
description: BITS transfère les fichiers uniquement lorsque le propriétaire du travail est connecté et qu’une connexion réseau est établie.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- BITS des connexions réseau
- transférer les BITS de tâche, propriété
- transférer les BITS de tâche, propriété, compte d’utilisateur
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7f841e3bf92004b62f3bbb576f71a45ac6b4a6bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102237"
---
# <a name="users-and-network-connections"></a>Utilisateurs et connexions réseau

BITS transfère les fichiers uniquement lorsque le propriétaire du travail est connecté et qu’une connexion réseau est établie. BITS traite la tâche de transfert à l’aide du contexte de sécurité du propriétaire du travail. L’utilisateur qui a créé le travail est considéré comme le propriétaire du travail. Toutefois, un utilisateur disposant de privilèges d’administrateur peut [**prendre possession**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) du travail d’un autre utilisateur.

Le service BITS interrompt un travail lorsque le propriétaire se déconnecte ou que la connexion réseau est perdue (BITS ne force pas de connexion réseau). Le service BITS reprend le travail lorsque le propriétaire ouvre à nouveau une session et qu’une connexion réseau est établie. Une fois la connexion réseau établie, un bref délai peut s’écouler avant que le service BITS ne commence à transférer des données.

En cas de perte de la connexion réseau, toutes les tâches dont l’État est mise en [**\_ \_ \_ file d’attente**](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou état du travail BG transféré sont déplacées vers l’état d' **\_ \_ \_ \_ erreur temporaire** de l’état de la tâche BG avec un code d’erreur [BG \_ E \_ réseau \_ déconnecté](bits-return-values.md) . **\_ \_ \_** Lorsqu’une connexion réseau est établie, tous les travaux dans un état d' **\_ \_ \_ \_ erreur temporaire d’état de travail BG** , qui peut inclure un code d’erreur, sont déplacés vers l’État en **\_ \_ \_ file d’attente d’état de la tâche BG** .

Pour que le service BITS détecte qu’un utilisateur a ouvert une session, l’utilisateur doit utiliser l’une des options de connexion interactives suivantes :

-   Connectez-vous via l’écran d’accueil.
-   Connectez-vous à un client de [service Terminal Server](../termserv/terminal-services-portal.md) .
-   Utilisez le [changement rapide d’utilisateur](../shell/fast-user-switching.md).
-   À compter de Windows 10, version 1607, connectez-vous à partir d’un autre appareil à l’aide de PowerShell à distance. Pour plus d’informations, consultez [pour gérer les sessions à distance PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md) .

L’exécution d’une application en tant qu’autre utilisateur (à l’aide de la commande **runas** ) n’est pas une ouverture de session interactive. Le service BITS n’exécutera pas les travaux associés à l’utilisateur spécifié.

Les comptes système LocalSystem, LocalService et NetworkService sont toujours connectés ; par conséquent, les travaux soumis par un service à l’aide de ces comptes s’exécutent toujours. Pour plus d’informations et pour connaître les limitations relatives à l’utilisation des comptes de service, consultez [comptes de service et bits](service-accounts-and-bits.md).

Les propriétaires de travaux peuvent fournir un jeton d’assistance à utiliser dans les situations où plusieurs jetons sont nécessaires pour effectuer un transfert, par exemple pour l’authentification avec un hôte distant. Pour plus d’informations, consultez [jetons d’assistance pour les tâches de transfert bits](helper-tokens-for-bits-transfer-jobs.md) . Dans les versions antérieures de Windows, le propriétaire du travail devait effectivement avoir des privilèges d’administrateur pour démarrer un travail qui utilisait un jeton d’assistance. Dans Windows 10, la version 1607, il est désormais possible pour un propriétaire de tâche BITS de définir des jetons d’assistance sans être administrateur, tant que le jeton d’assistance ne dispose pas de fonctionnalités d’administrateur. Cela réduit l’espace de vulnérabilité des outils de mise à jour ou de téléchargement en arrière-plan en leur permettant de s’exécuter sur le compte NetworkService avec le moins de privilèges plutôt que sur un compte doté de privilèges administrateur.

Les utilisateurs disposant d’un [jeton restreint](../secauthz/restricted-tokens.md) (un jeton qui contient des SID de restriction) ne peuvent pas créer ou modifier des travaux.
 

 