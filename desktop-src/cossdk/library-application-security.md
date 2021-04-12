---
description: Étant donné qu’une application de bibliothèque COM+ est hébergée par un autre processus, qui peut avoir ses propres paramètres de sécurité, la sécurité pour les applications de bibliothèque nécessite une attention particulière.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sécurité de l’application de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523420"
---
# <a name="library-application-security"></a>Sécurité de l’application de bibliothèque

Étant donné qu’une application de bibliothèque COM+ est hébergée par un autre processus, qui peut avoir ses propres paramètres de sécurité, la sécurité pour les applications de bibliothèque nécessite une attention particulière.

Les contraintes suivantes s’appliquent à la sécurité de l’application de bibliothèque :

-   Les applications de bibliothèque s’exécutent sous le jeton de sécurité du processus client plutôt que sous leur propre identité d’utilisateur. Ils n’ont que peu de privilèges que le client a.
-   Les applications de bibliothèque ne contrôlent pas la sécurité au niveau du processus. Aucun utilisateur dans les rôles n’est ajouté au descripteur de sécurité pour le processus. La seule façon pour une application de bibliothèque d’effectuer ses propres contrôles d’accès consiste à utiliser la sécurité au niveau du composant. (Voir [limites de sécurité](security-boundaries.md).)
-   Les applications de bibliothèque peuvent être configurées de façon à participer ou non à l’authentification du processus hôte, en activant ou désactivant l’authentification. (Voir [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).)
-   Les applications de bibliothèque ne peuvent pas définir un niveau d’emprunt d’identité ; ils utilisent ce processus hôte.

## <a name="using-library-applications-to-limit-application-privilege"></a>Utilisation d’applications de bibliothèque pour limiter le privilège de l’application

Dans certains cas, vous souhaiterez peut-être configurer une application en tant qu’application de bibliothèque de manière à ce qu’elle s’exécute sous l’identité du processus d’hébergement. Cela limite fondamentalement l’application afin qu’elle puisse accéder uniquement aux ressources auxquelles son client, le processus hôte, peut accéder. Les threads sur lesquels s’exécutent les composants d’application de bibliothèque utilisent le jeton de processus par défaut. par conséquent, lorsqu’ils effectuent des appels en dehors de l’application ou accèdent à des ressources telles que des fichiers protégés par un descripteur de sécurité, ils semblent être le client. Pour les applications qui effectuent des tâches sensibles, il peut s’agir d’un moyen simple de contrôler l’étendue de leurs actions.

## <a name="effectively-securing-library-applications"></a>Sécurisation efficace des applications de bibliothèque

Il existe des considérations spéciales relatives à la configuration de la sécurité basée sur les rôles et de l’authentification pour les applications de bibliothèque afin qu’elles s’exécutent comme prévu. Pour plus d’informations, consultez [configuration de la sécurité pour les applications de bibliothèque](configuring-security-for-library-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> <dt>

[Utilisation de la stratégie de restriction logicielle dans COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



