---
description: Si votre application COM+ utilise la sécurité basée sur les rôles, vous devez effectuer plusieurs tâches.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configuration de la sécurité de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915695"
---
# <a name="configuring-role-based-security"></a>Configuration de la sécurité de Role-Based

Si votre application COM+ utilise la sécurité basée sur les rôles, vous devez effectuer plusieurs tâches. Lors de la conception des composants de votre application, vous définissez les rôles nécessaires pour protéger l’accès à ces composants. Vous pouvez également choisir les rôles à assigner aux composants, interfaces et méthodes de l’application. Pendant l’intégration de l’application, vous utilisez l’outil d’administration Services de composants pour ajouter les rôles définis à l’application et assigner chaque rôle aux composants, interfaces et méthodes appropriés.

Dans Configuration de la sécurité basée sur les rôles, procédez comme suit :

1.  Activez les vérifications d’accès au niveau de l’application. Pour activer la vérification de la sécurité pour une application. Pour plus d’informations sur l’exécution de cette étape, consultez [activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md) .
2.  Définissez le niveau de sécurité pour les vérifications d’accès. Pour définir la sécurité au niveau du processus ou au niveau du processus et du composant. Pour plus d’informations sur l’exécution de cette étape, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md) .
3.  Activez les vérifications d’accès au niveau du composant. Pour activer la vérification de la sécurité au niveau du composant, de l’interface et de la méthode. Pour plus d’informations sur l’exécution de cette étape, consultez [activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md) .
4.  Définir des rôles pour une application. Pour créer des rôles pour une application. Pour plus d’informations sur l’exécution de cette étape, consultez [définition de rôles pour une application](defining-roles-for-an-application.md) .
5.  Assignez des rôles à des composants, des interfaces ou des méthodes. Pour assigner des rôles à des ressources spécifiques au sein d’une application. Pour plus d’informations sur l’exécution de cette étape [, consultez assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de la stratégie de restriction logicielle](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Définition d’un niveau d’emprunt d’identité](setting-an-impersonation-level.md)
</dt> </dl>

 

 



