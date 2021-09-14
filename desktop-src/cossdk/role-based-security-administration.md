---
description: Administration de la sécurité Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administration de la sécurité Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922920"
---
# <a name="role-based-security-administration"></a>Administration de la sécurité Role-Based

La sécurité basée sur les rôles est un service automatique fourni par COM+ qui vous permet de construire et d’appliquer de manière administrative une stratégie de contrôle d’accès pour votre application COM+. Avec un modèle de configuration de sécurité flexible et extensible, la sécurité basée sur les rôles offre un avantage considérable sur l’application de la sécurité dans vos composants et offre les avantages suivants :

-   Vous pouvez configurer la sécurité de manière administrative à l’aide de l’outil d’administration Services de composants ou des fonctions d’administration.
-   Vous n’avez pas besoin d’écrire une logique relative à la sécurité dans vos composants lorsque la protection des rôles au niveau de la méthode vous offre un contrôle d’accès suffisamment précis.
-   Vous n’avez pas besoin de factoriser la sécurité dans la conception de l’interface ou du composant. Au lieu de cela, vous pouvez définir la sécurité par méthode.
-   Vous pouvez vous concentrer sur la structure de la stratégie de sécurité que vous souhaitez appliquer et, par le biais des rôles, cette stratégie peut être clairement exprimée aux administrateurs qui déploient votre application.
-   Vous pouvez facilement modifier une stratégie de sécurité pour l’adapter aux exigences de sécurité en constante évolution pour une application.
-   Vous pouvez créer des stratégies de sécurité plus granulaires par programmation, si nécessaire, à l’aide de la sécurité basée sur les rôles comme plateforme de prise en charge.
-   Vous pouvez tirer parti de la sécurité basée sur les rôles pour effectuer un audit détaillé, car vous pouvez obtenir des informations de sécurité de l’appelant pour une chaîne entière d’appels en amont.

> [!Note]  
> Les utilisateurs du rôle administrateur pour l’application système doivent être membres du groupe Administrateurs local. en outre, à partir de Windows Server 2003, la fonctionnalité d’authentification de l’Application système COM+ comprend la valeur EOAC \_ DISABLE \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

 

Consultez les rubriques suivantes de cette section pour plus d’informations sur le fonctionnement de la sécurité basée sur les rôles et sur les points à prendre en compte lors de l’utilisation de cette stratégie de sécurité pour créer une stratégie de sécurité pour une application :

-   [Utilisation de rôles pour l’autorisation du client](using-roles-for-client-authorization.md)
-   [Conception efficace des rôles](designing-roles-effectively.md)
-   [Limites de sécurité](security-boundaries.md)
-   [Informations de contexte de l’appel de sécurité](security-call-context-information.md)
-   [Propriété de contexte de sécurité](security-context-property.md)

Pour obtenir des descriptions détaillées des étapes nécessaires à la configuration de la sécurité basée sur les rôles pour une application, consultez Configuration de la [sécurité des Role-Based](configuring-role-based-security.md).

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

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Utilisation de la stratégie de restriction logicielle dans COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
