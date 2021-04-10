---
description: Un service (ou tout processus s’exécutant dans un contexte de sécurité différent) qui doit accéder à une ressource distante doit utiliser le nom UNC (Universal Naming Convention) pour accéder à la ressource.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Services et lecteurs redirigés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b1435e69ded3bf13a0869a0b9ad2b90bb4682c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952876"
---
# <a name="services-and-redirected-drives"></a>Services et lecteurs redirigés

Un service (ou tout processus s’exécutant dans un contexte de sécurité différent) qui doit accéder à une ressource distante doit utiliser le nom UNC (Universal Naming Convention) pour accéder à la ressource. Le service doit disposer des privilèges appropriés pour accéder à la ressource. Si un service côté serveur utilise une connexion RPC, la délégation doit être activée sur le serveur distant.

Les lettres de lecteur ne sont pas globales pour le système. Chaque session de connexion reçoit son propre ensemble de lettres de lecteur de A à Z. Par conséquent, les lecteurs redirigés ne peuvent pas être partagés entre des processus s’exécutant sous des comptes d’utilisateur différents. En outre, un service (ou tout processus s’exécutant au sein de sa propre session de connexion) ne peut pas accéder aux lettres de lecteur qui ont été établies au cours d’une session de connexion différente.

Un service ne doit pas accéder directement aux ressources réseau ou locales par le biais de lettres de lecteur mappées, ni appeler la commande **net use** pour mapper les lettres de lecteur au moment de l’exécution. La commande **net use** n’est pas recommandée pour plusieurs raisons :

-   Les mappages de lecteur sont disponibles dans les contextes d’ouverture de session. par conséquent, si une application s’exécute dans le contexte du [compte LocalService](localservice-account.md), tout autre service s’exécutant dans ce contexte peut avoir accès au lecteur mappé.
-   Si le service fournit des informations d’identification explicites à une commande **net use** , ces informations d’identification peuvent être partagées par inadvertance en dehors des limites de service. Au lieu de cela, le service doit utiliser l' [emprunt d’identité du client](/windows/desktop/SecAuthZ/client-impersonation) pour emprunter l’identité de l’utilisateur.
-   Plusieurs services exécutés dans le même contexte peuvent interférer entre eux. Si les deux services effectuent une **utilisation net** explicite et fournissent les mêmes informations d’identification en même temps, un service échoue et une erreur « déjà connecté » s’affiche.

En outre, un service ne doit pas utiliser les [fonctions de réseau Windows](/windows/desktop/WNet/windows-networking-functions) pour gérer les lettres de lecteur mappées. Bien que les fonctions WNet puissent retourner avec succès, le comportement qui en résulte n’est pas le même que prévu. Lorsque le système établit un lecteur Redirigé, il est stocké par utilisateur. Seul l’utilisateur est en mesure de gérer le lecteur Redirigé. Le système effectue le suivi des lecteurs redirigés en fonction de l’identificateur de sécurité (SID) d’ouverture de session de l’utilisateur. Le SID d’ouverture de session est un identificateur unique pour la session d’ouverture de session de l’utilisateur. Un seul utilisateur peut avoir plusieurs sessions d’ouverture de session simultanées sur le système.

Si un service est configuré pour s’exécuter sous un compte d’utilisateur, le système crée toujours une nouvelle session d’ouverture de session pour l’utilisateur et démarre le service dans cette nouvelle session. Par conséquent, un service ne peut pas gérer les mappages de lecteur établis dans les autres sessions de l’utilisateur.

**Windows Server 2003 :** Sur un ordinateur doté de plusieurs interfaces réseau (autrement dit, un ordinateur multirésident), un délai pouvant atteindre 60 secondes peut se produire lors de l’utilisation de chemins d’accès UNC pour accéder aux fichiers stockés sur un serveur SMB (Server Message Block) distant. Pour plus d’informations, voir l' [article 890553](https://support.microsoft.com/kb/890553) de la base de connaissances d’aide et de support.

 

 
