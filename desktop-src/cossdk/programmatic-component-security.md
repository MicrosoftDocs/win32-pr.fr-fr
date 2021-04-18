---
description: Lorsque vous utilisez la sécurité basée sur les rôles dans l’application COM+ qui contient votre composant, vous avez accès aux fonctionnalités de sécurité par programmation à partir de votre composant.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sécurité des composants de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515937"
---
# <a name="programmatic-component-security"></a>Sécurité des composants de programmation

Lorsque vous utilisez la sécurité basée sur les rôles dans l’application COM+ qui contient votre composant, vous avez accès aux fonctionnalités de sécurité par programmation à partir de votre composant. Vous pouvez vérifier l’appartenance à un rôle pour déterminer si certaines sections de code sont exécutées, vous pouvez accéder à des informations de sécurité à l’aide de l’objet de contexte d’appel de sécurité et vous pouvez déterminer si la sécurité est activée pour l’appel en cours. Vous pouvez effectuer toutes ces tâches à l’aide d’une référence à un objet [**SecurityCallContext**](securitycallcontext.md) (pour les applications Microsoft Visual Basic) ou d’un pointeur vers l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (pour les applications C et Microsoft Visual C++).

Pour plus d’informations sur la sécurité basée sur les rôles par programmation, consultez les rubriques suivantes dans cette section :

-   [Vérification de l’appartenance au rôle](checking-role-membership.md)
-   [Détermination de l’activation ou non de la sécurité Role-Based](determining-whether-role-based-security-is-enabled.md)
-   [Accès aux informations de contexte de l’appel de sécurité](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>Emprunt d’identité et fonctionnalités de sécurité COM

Si votre composant est utilisé dans une application COM+ qui n’utilise pas la sécurité basée sur les rôles, la vérification des rôles par programme et les informations de contexte d’appel de sécurité ne sont pas disponibles. Toutefois, vous pouvez utiliser la fonctionnalité de sécurité par programme fournie par COM. Pour plus d’informations, consultez [sécurité dans com](/windows/desktop/com/security-in-com).

Bien que vous puissiez utiliser la plupart des fonctionnalités de sécurité fournies par COM, vous ne pouvez pas appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) à partir d’un composant qui fait partie d’une application com+, car **CoInitializeSecurity** est appelé par le substitut dans lequel l’application com+ s’exécute. Toutefois, vous pouvez appeler d’autres fonctions de sécurité, telles que [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), qui récupère des informations sur le client.

En particulier, lorsque vous devez utiliser l’identité du client pour accéder à certaines ressources (par exemple, accéder à un fichier protégé par un descripteur de sécurité ou propager l’identité du client via vers une base de données), vous pouvez effectuer l’emprunt d’identité par programmation. Pour plus d’informations sur le moment et la façon de procéder, consultez [emprunt d’identité du client et délégation](client-impersonation-and-delegation.md).

## <a name="testing-security-functionality"></a>Test de la fonctionnalité de sécurité

Si vous utilisez la sécurité par programmation COM+ dans votre composant, vous devez intégrer le composant dans une application COM+ lorsque vous êtes prêt à tester les fonctionnalités de sécurité du composant. Si un composant qui utilise la sécurité COM+ est exécuté sans être intégré à une application COM+, les exceptions sont levées. Par conséquent, si vous souhaitez vous assurer qu’un tel composant peut également être intégré à une application qui ne fait pas partie de l’environnement COM+, vous devez vous assurer que ces exceptions sont gérées correctement.

## <a name="documenting-security-requirements"></a>Documentation des exigences de sécurité

Si vous écrivez un composant autonome pour les applications COM+ qui utilisent la sécurité basée sur les rôles, vous devez documenter le composant afin que la sécurité puisse être configurée de manière appropriée lorsque le composant est intégré à une application COM+. Par exemple, vous devez identifier les rôles qui doivent être ajoutés et expliquer à quelles méthodes et interfaces chaque rôle doit être assigné. En outre, si une méthode telle que IsCallerInRole (« Teller ») est appelée, vous devez décrire les fonctionnalités auxquelles seuls les demandeurs ont accès. Vous devez également spécifier si un rôle est requis pour aider à protéger l’accès à l’ensemble du composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sécurité de l’application de bibliothèque](library-application-security.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> <dt>

[Utilisation de la stratégie de restriction logicielle dans COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
