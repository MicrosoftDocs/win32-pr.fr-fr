---
description: La sécurité est vérifiée uniquement au niveau des limites de l’application.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Limites de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050be064c8a2fe3dc8eb81e2297e1699504f92ae7b8b4352d9b875dfc50e91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047267"
---
# <a name="security-boundaries"></a>Limites de sécurité

La sécurité est vérifiée uniquement au niveau des limites de l’application. Autrement dit, pour deux composants de la même application, lorsqu’un composant appelle l’autre, aucune vérification de la sécurité n’est effectuée. Toutefois, si deux applications partagent le même processus et qu’un composant dans un appelle un composant de l’autre, une vérification de la sécurité est effectuée car une limite d’application est franchie. De même, si deux applications résident dans des processus serveur différents et qu’un composant de la première application appelle un composant dans la deuxième application, une vérification de la sécurité est effectuée.

Par conséquent, si vous avez deux composants et que vous souhaitez que les contrôles de sécurité soient effectués quand l’un appelle l’autre, vous devez placer les composants dans des applications COM+ distinctes.

Étant donné que les applications de bibliothèque COM+ sont hébergées par d’autres processus, il existe une limite de sécurité entre l’application de bibliothèque et le processus d’hébergement. En outre, l’application de bibliothèque ne contrôle pas la sécurité au niveau du processus, ce qui affecte la façon dont vous devez configurer la sécurité pour celle-ci. Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).

Déterminer si un contrôle de sécurité doit être effectué sur un appel dans un composant est basé sur la propriété de sécurité du contexte de l’objet créé lorsque le composant configuré est instancié. Pour plus d’informations, consultez [Security Context Property](security-context-property.md).

## <a name="component-level-access-checks"></a>Contrôles d’accès aux Component-Level

Pour une application serveur COM+, vous avez la possibilité d’appliquer des vérifications d’accès au niveau du composant ou au niveau du processus.

Lorsque vous sélectionnez le contrôle d’accès au niveau du composant, vous activez les attributions de rôles affinées. Vous pouvez assigner des rôles à des composants, des interfaces et des méthodes, et obtenir une stratégie d’autorisation articulée. Il s’agit de la configuration standard pour les applications utilisant la sécurité basée sur les rôles.

Pour les applications de bibliothèque COM+, vous devez sélectionner sécurité au niveau du composant si vous souhaitez utiliser des rôles. Les applications de bibliothèque ne peuvent pas utiliser la sécurité au niveau du processus.

Vous devez sélectionner contrôle d’accès au niveau du composant si vous utilisez la sécurité basée sur les rôles par programmation. Les informations de contexte de l’appel de sécurité sont disponibles uniquement lorsque la sécurité au niveau du composant est activée. Pour plus d’informations, consultez informations de contexte de l' [appel de sécurité](security-call-context-information.md).

En outre, lorsque vous sélectionnez le contrôle d’accès au niveau du composant, la propriété de sécurité sera incluse dans le contexte de l’objet. Cela signifie que la configuration de la sécurité peut jouer un rôle dans la façon dont l’objet est activé. Pour plus d’informations, consultez [Security Context Property](security-context-property.md).

## <a name="process-level-access-checks"></a>Contrôles d’accès aux Process-Level

Les vérifications au niveau du processus s’appliquent uniquement à la limite de l’application. Autrement dit, les rôles que vous avez définis pour l’application COM+ entière déterminent qui est autorisé à accéder à n’importe quelle ressource au sein de l’application. Aucune attribution de rôle plus fine n’est appliquée. Les rôles sont essentiellement utilisés pour créer un descripteur de sécurité par rapport auquel tout appel dans les composants de l’application est validé. Dans ce cas, vous ne souhaitez pas construire une stratégie d’autorisation détaillée avec plusieurs rôles. L’application utilisera un descripteur de sécurité unique.

Pour les applications de bibliothèque COM+, vous ne devez pas sélectionner les contrôles d’accès au niveau du processus. L’application de bibliothèque s’exécutera dans le processus du client et ne contrôlera donc pas la sécurité au niveau du processus. Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).

Lorsque les vérifications d’accès au niveau du processus sont activées, les informations de contexte de l’appel de sécurité ne sont pas disponibles. Cela signifie que vous ne pouvez pas effectuer de sécurité par programmation lorsque vous utilisez uniquement la sécurité au niveau du processus. Pour plus d’informations, consultez informations de contexte de l' [appel de sécurité](security-call-context-information.md).

En outre, la propriété de sécurité ne sera pas incluse dans le contexte de l’objet. Cela signifie que lorsque vous utilisez uniquement des vérifications d’accès au niveau du processus, la configuration de la sécurité ne jouera jamais un rôle dans la façon dont l’objet est activé. Pour plus d’informations, consultez [Security Context Property](security-context-property.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception efficace des rôles](designing-roles-effectively.md)
</dt> <dt>

[Informations de contexte de l’appel de sécurité](security-call-context-information.md)
</dt> <dt>

[Propriété de contexte de sécurité](security-context-property.md)
</dt> <dt>

[Utilisation de rôles pour l’autorisation du client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



