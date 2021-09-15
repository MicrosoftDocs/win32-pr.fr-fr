---
description: Conception pour la sécurité
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Conception pour la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519344"
---
# <a name="designing-for-security"></a>Conception pour la sécurité

Votre stratégie de bout en bout pour la sécurité dépend évidemment du type d’application distribuée que vous développez. Voici plusieurs suggestions pour résoudre la sécurité en ce qui concerne la logique d’application de couche intermédiaire :

-   Pour obtenir de l’efficacité et des performances, authentifiez-vous comme vous le souhaitez. Si votre application implique une architecture de la logique du navigateur au niveau de la base de données, envisagez de mapper les clients du navigateur aux identités de domaine, d’exécuter l’application COM+ avec des identités spécifiques à chaque application et de configurer les tables de la couche données pour qu’elles soient accessibles uniquement par une identité d’application particulière. Ce scénario de serveur approuvé est plus évolutif et moins problématique que l’utilisation du SGBD pour l’authentification.
-   Si vous concevez un composant qui sera utilisé dans une application distribuée à l’aide de la sécurité basée sur les rôles, vous pouvez utiliser la fonctionnalité de [sécurité com+](com--security.md) . Cette fonctionnalité vous permet d’appeler des méthodes telles que [**IObjectContext :: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) et [**IObjectContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) pour aider à protéger des blocs de code d’un accès non autorisé. Vous pouvez également utiliser le contexte de l’appel de sécurité pour obtenir des informations sur les appelants d’un objet.
-   Si vous concevez un composant qui sera utilisé dans une application distribuée sans utiliser la sécurité basée sur les rôles, la sécurité est automatiquement vérifiée uniquement au niveau du processus. Les autorisations de processus d’accès déterminent qui est autorisé à accéder à l’application. Si vous avez besoin d’un contrôle plus fin sur les paramètres de sécurité au niveau du processus ou au niveau de l’interface, utilisez la fonctionnalité de sécurité par programme fournie par COM.
-   Si un composant qui utilise la sécurité COM+ est exécuté sans être intégré à une application COM+, les exceptions sont levées. Par conséquent, si vous souhaitez que ce composant soit correctement intégré à une application qui ne fait pas partie de l’environnement COM+, vous devez gérer toutes les exceptions de manière appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception pour la disponibilité](designing-for-availability.md)
</dt> <dt>

[Conception pour le déploiement](designing-for-deployment.md)
</dt> <dt>

[Conception pour l’évolutivité](designing-for-scalability.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> </dl>

 

 



