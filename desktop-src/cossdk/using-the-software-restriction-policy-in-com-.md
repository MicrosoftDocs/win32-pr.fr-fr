---
description: L’utilisation correcte de la stratégie de restriction logicielle peut rendre votre entreprise plus agile, car elle fournit une infrastructure proactive pour empêcher les problèmes, plutôt qu’une infrastructure réactive qui s’appuie sur l’alternative coûteuse de la restauration d’un système après un problème. La stratégie de restriction logicielle a été introduite dans la version de Microsoft Windows XP pour aider à protéger les systèmes contre du code inconnu et potentiellement dangereux. La stratégie de restriction fournit un mécanisme dans lequel seul le code de confiance est autorisé à accéder de façon illimitée aux privilèges d’un utilisateur. Un code inconnu, qui peut contenir des virus ou du code qui est en conflit avec des programmes actuellement installés, est autorisé à s’exécuter uniquement dans un environnement restreint (souvent appelé bac à sable (sandbox)) où il n’est pas autorisé à accéder à des privilèges d’utilisateur sensibles à la sécurité.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Utilisation de la stratégie de restriction logicielle dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483408"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Utilisation de la stratégie de restriction logicielle dans COM+

L’utilisation correcte de la stratégie de restriction logicielle peut rendre votre entreprise plus agile, car elle fournit une infrastructure proactive pour empêcher les problèmes, plutôt qu’une infrastructure réactive qui s’appuie sur l’alternative coûteuse de la restauration d’un système après un problème. La stratégie de restriction logicielle a été introduite dans la version de Microsoft Windows XP pour aider à protéger les systèmes contre du code inconnu et potentiellement dangereux. La stratégie de restriction fournit un mécanisme dans lequel seul le code de confiance est autorisé à accéder de façon illimitée aux privilèges d’un utilisateur. Un code inconnu, qui peut contenir des virus ou du code qui est en conflit avec des programmes actuellement installés, est autorisé à s’exécuter uniquement dans un environnement restreint (souvent appelé *bac à sable (sandbox*)) où il n’est pas autorisé à accéder à des privilèges d’utilisateur sensibles à la sécurité.

La stratégie de restriction logicielle dépend de l’attribution de niveaux de confiance au code qui peut s’exécuter sur un système. Actuellement, il existe deux niveaux de confiance : non restreint et interdit. Le code ayant un niveau de confiance non restreint bénéficie d’un accès illimité aux privilèges de l’utilisateur. ce niveau de confiance ne doit donc être appliqué qu’à du code d’un niveau de confiance suffisant. Le code avec un niveau de confiance interdit n’est pas autorisé à accéder à des privilèges d’utilisateur sensibles à la sécurité et peut s’exécuter uniquement dans un bac à sable (sandbox) qui permet d’empêcher du code non restreint de charger le code non autorisé dans son espace d’adressage.

La configuration de la stratégie de restriction logicielle pour un système s’effectue par le biais de l’outil d’administration stratégie de sécurité locale, tandis que la configuration de la stratégie de restriction des applications COM+ individuelles est effectuée par programmation ou par le biais de l’outil d’administration Services de composants. Si le niveau de confiance de la stratégie de restriction n’est pas spécifié pour une application COM+, les paramètres du système sont utilisés pour déterminer le niveau de confiance de l’application. Les paramètres de stratégie de restriction COM+ doivent être soigneusement coordonnés avec les paramètres du système, car une application COM+ ayant un niveau de confiance illimité peut charger uniquement des composants avec un niveau de confiance illimité. une application COM+ non autorisée peut charger des composants avec n’importe quel niveau de confiance, mais ne peut pas accéder à tous les privilèges de l’utilisateur.

Outre les niveaux de confiance de la stratégie de restriction logicielle des applications COM+ individuelles, deux autres propriétés déterminent la façon dont la stratégie de restriction est utilisée pour toutes les applications COM+. Si [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) est activé, les tentatives de connexion aux objets en cours d’exécution sont vérifiées. L’objet en cours d’exécution ne peut pas avoir un niveau de confiance moins strict que l’objet client. Par exemple, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance non autorisé si l’objet client a un niveau de confiance illimité.

La deuxième propriété détermine la façon dont la stratégie de restriction logicielle gère les connexions d’activation en tant qu’activateur. Si [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) est activé, le niveau de confiance configuré pour l’objet serveur est comparé au niveau de confiance de l’objet client et le niveau de confiance le plus strict est utilisé pour exécuter l’objet serveur. Si SRPActivateAsActivatorChecks n’est pas activé, l’objet serveur s’exécute avec le niveau de confiance de l’objet client, quel que soit le niveau de confiance avec lequel il a été configuré. Par défaut, SRPRunningObjectChecks et SRPActivateAsActivatorChecks sont activés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Configuration de la stratégie de restriction logicielle](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Sécurité de l’application de bibliothèque](library-application-security.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> </dl>

 

 
