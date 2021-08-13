---
description: Des considérations particulières sont à prendre en compte lors de la configuration de la sécurité basée sur les rôles et de l’authentification pour les applications de bibliothèque.
ms.assetid: 1117ac64-653d-4640-97cd-f37b0949dc57
title: Configuration de la sécurité pour les applications de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0d8b3993a00512c20409f1f029b7402d5f9ace97984cbe9757453b5672125f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548882"
---
# <a name="configuring-security-for-library-applications"></a>Configuration de la sécurité pour les applications de bibliothèque

Des considérations particulières sont à prendre en compte lors de la configuration de la sécurité basée sur les rôles et de l’authentification pour les applications de bibliothèque.

## <a name="enabling-or-disabling-authentication"></a>Activation ou désactivation de l’authentification

L’un des facteurs à prendre en compte est de savoir si les appelants de l’application de bibliothèque doivent être soumis aux vérifications de sécurité au niveau du processus du processus d’hébergement, c’est-à-dire s’il faut activer ou désactiver l’authentification.

Par exemple, si l’application de bibliothèque doit être hébergée par un navigateur, il peut être nécessaire de recevoir des rappels non authentifiés. Pour répondre à ce besoin, vous pouvez désactiver l’authentification afin que le processus d’hébergement n’effectue pas de vérifications de sécurité pour les appelants de l’application de bibliothèque. Lorsque vous désactivez l’authentification, l’application de la bibliothèque n’est pas authentifiée, tous les appels à celle-ci sont correctement effectués. Les appelants de l’application de bibliothèque ne sont pas soumis aux vérifications de sécurité du processus d’hébergement. Fondamentalement, l’application de bibliothèque est marquée comme « non authentifiée » et les vérifications de sécurité sont omises pour les appels à l’application de bibliothèque.

Pour plus d’informations sur l’activation ou la désactivation de l’authentification, consultez [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).

## <a name="enforcing-role-checks"></a>Application des vérifications des rôles

Une autre décision à prendre est de déterminer si l’application de bibliothèque doit utiliser la [sécurité basée sur les rôles](role-based-security-administration.md). Si la sécurité basée sur les rôles est utilisée, vous devez utiliser la sécurité au niveau du composant pour effectuer toutes les vérifications d’accès. Les rôles attribués à l’application de bibliothèque ne sont pas reflétés dans le descripteur de sécurité de processus. La seule autorisation que l’application de bibliothèque peut contrôler est au niveau du composant. Pour plus d’informations sur la sécurité au niveau du composant, consultez [limites de sécurité](security-boundaries.md).

Pour savoir comment définir la sécurité au niveau du composant, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).

## <a name="configuration-scenarios"></a>Scénarios de configuration

Pour mieux comprendre les implications de l’utilisation de la sécurité basée sur les rôles par l’application de bibliothèque et pour déterminer si l’application de la bibliothèque doit être non authentifiée, envisagez les scénarios suivants :

-   **L’authentification est activée et la sécurité basée sur les rôles est utilisée.** Dans ce scénario, les contrôles de sécurité sont effectués par le processus d’hébergement et certains appelants se voient refuser l’accès au niveau du processus. En outre, la vérification des rôles est effectuée au niveau de l’application de la bibliothèque afin que certains appelants qui le font via la vérification de la sécurité au niveau du processus se voient refuser l’accès à l’application de bibliothèque lorsque l’appartenance au rôle est vérifiée. Il s’agit du scénario habituel pour une application de bibliothèque COM+ qui utilise la sécurité basée sur les rôles.

    L’illustration suivante montre le scénario dans lequel l’authentification est activée et l’utilisation de la vérification des rôles.

    ![Diagramme qui montre l’authentification effectuée au sein d’un processus hôte.](images/18004ed7-e95e-4c66-9e17-f163cdeefd71.png)

-   **L’authentification est activée et la sécurité basée sur les rôles n’est pas utilisée.** Dans ce scénario, les vérifications de sécurité sont effectuées au niveau du processus, mais l’appartenance au rôle n’est pas vérifiée au niveau de l’application de la bibliothèque. Par conséquent, tout appelant de l’application de bibliothèque qui le fait via la vérification de la sécurité au niveau du processus aura accès à l’application de bibliothèque, car l’appartenance au rôle n’est pas vérifiée. Cette situation se présente quand une application COM qui n’utilise pas la sécurité basée sur les rôles est migrée vers une application de bibliothèque COM+.

    L’illustration suivante montre le scénario dans lequel l’authentification est activée et que la vérification des rôles n’est pas utilisée.

    ![Diagramme qui montre l’authentification au niveau du processus pour une application de bibliothèque au sein du processus hôte.](images/3e5a64c6-39a9-4ff7-b084-8396fe779210.png)

-   **L’authentification est désactivée et la sécurité basée sur les rôles est utilisée.** Dans ce scénario, les vérifications de sécurité sont effectuées au niveau du processus, mais les appelants à l’application de bibliothèque ne sont pas authentifiés. En effet, les appelants de l’application de bibliothèque sont exemptés de la vérification de la sécurité au niveau du processus. Étant donné que la vérification des rôles est activée, l’appartenance au rôle détermine qui est autorisé à accéder à l’application de bibliothèque. Ce scénario peut être approprié lorsque la vérification de sécurité qui serait effectuée par le processus d’hébergement est trop restrictive, mais que vous devez avoir une restriction d’accès sur l’application de bibliothèque ou sur des interfaces ou des méthodes spécifiques. Ce scénario vous permet de désactiver efficacement la sécurité des processus et de bénéficier d’une vérification d’accès de niveau appropriée à l’aide de la sécurité basée sur les rôles.

    L’illustration suivante montre le scénario dans lequel l’authentification est désactivée et la vérification des rôles en cours d’utilisation.

    ![Diagramme illustrant la « vérification de l’appartenance à un rôle » dans une application de bibliothèque au sein d’un processus hôte.](images/e0cc604c-ba86-4087-9a74-1b6fdce8d69a.png)

-   **L’authentification est désactivée et la sécurité basée sur les rôles n’est pas utilisée.** Dans ce scénario, les contrôles de sécurité sont toujours effectués au niveau du processus, mais comme dans le scénario précédent, les appelants de l’application de bibliothèque réussissent toujours cette vérification de sécurité. Étant donné que la vérification des rôles est également désactivée, l’appartenance au rôle n’est pas vérifiée au niveau de l’application de la bibliothèque. Pour l’essentiel, tout le monde peut appeler l’application de bibliothèque. ce scénario doit être choisi lorsque votre objet COM doit recevoir des rappels non authentifiés, comme cela peut être le cas avec un contrôle de ActiveX hébergé par Internet Explorer et avec un composant logiciel enfichable mmc (Microsoft Management Console). Bien entendu, cet objet COM doit être approuvé pour se comporter de manière appropriée lors de la réception d’appels non authentifiés. Par exemple, il ne doit pas accéder à des fichiers arbitraires pour le compte de ses appelants.

    Le scénario dans lequel l’authentification est désactivée et la vérification des rôles n’est pas utilisée est indiqué dans l’illustration suivante.

    ![Diagramme qui montre les appels à une application de bibliothèque qui ne sont pas authentifiés dans le processus hôte.](images/df3c9a02-52dd-4e07-a5f1-76cef0dab5cb.png)

Une fois que vous avez décidé d’activer ou de désactiver l’authentification pour votre application de bibliothèque COM+, consultez [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md) pour obtenir une procédure pas à pas qui explique comment désactiver (ou activer) l’authentification à l’aide de l’outil d’administration Services de composants. Si votre application de bibliothèque utilise la sécurité basée sur les rôles, consultez Configuration de la [sécurité de Role-Based](configuring-role-based-security.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité de l’application de bibliothèque](library-application-security.md)
</dt> </dl>

 

 



