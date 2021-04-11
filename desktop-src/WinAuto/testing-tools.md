---
title: Outils de test
description: Décrit les outils de test de l’implémentation de l’accessibilité de votre application pour s’assurer que l’interface utilisateur est entièrement accessible aux applications clientes et aux utilisateurs qui accèdent à votre application via le clavier.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- outils de test d’accessibilité
- outils de test, accessibilité
- test d’accessibilité
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102257"
---
# <a name="testing-tools"></a>Outils de test

L’accès par programme et l’accès au clavier sont des exigences critiques pour la prise en charge de l’accessibilité dans votre application. Sans un accès adéquat, de nombreux utilisateurs de la technologie d’assistance (AT), tels que le lecteur d’écran et les utilisateurs du clavier visuel, ne peuvent pas utiliser votre application. Veillez à tester minutieusement l’implémentation de l’accessibilité de votre application pour confirmer qu’elle fournit des informations adéquates sur ses éléments d’interface utilisateur, et que tous les scénarios de votre application peuvent être atteints uniquement avec le clavier.

Outre la vérification de l’accès par programme, certains outils peuvent vous aider à évaluer l’implémentation de l’accès au clavier de votre application. Toutefois, les outils seuls ne sont pas suffisants. Il est important de vérifier manuellement que tous les scénarios peuvent être atteints uniquement avec le clavier.

Pour les exigences de programmation et de clavier, aucun outil ne peut vérifier votre implémentation complète. Essayez d’utiliser un grand nombre d’outils pour vérifier votre implémentation et, lorsque cela est possible, recherchez des utilisateurs de technologies d’assistance, telles que les lecteurs d’écran, pour utiliser votre interface utilisateur.

Cette section décrit les outils disponibles pour tester les implémentations de Microsoft UI Automation (UIA) et de Microsoft Active Accessibility (MSAA).

## <a name="tools"></a>Outils

Informations [d’accessibilité](https://accessibilityinsights.io/) : aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les applications Web et Windows.

- [Accessibility Insights pour le Web](https://accessibilityinsights.io/docs/web/overview) est une extension pour chrome et [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) qui aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les sites et les applications Web. Il prend en charge deux scénarios principaux :
  - **FastPass** : processus léger et en deux étapes qui aide les développeurs à identifier les problèmes d’accessibilité courants et à fort impact en moins de cinq minutes.  
  - **Évaluation** : permet à quiconque de vérifier qu’un site Web est compatible 100% avec les normes et les consignes d’accessibilité. [Accessibility Insights](https://accessibilityinsights.io/) vous permet également de passer en revue les éléments, les propriétés, les modèles de contrôle et les événements UI Automation (comme les outils hérités [Inspect](/windows/desktop/winauto/inspect-objects) et [AccEvent](/windows/desktop/winauto/accessible-event-watcher) décrits dans la section suivante).

- [Accessibility Insights pour Windows](https://accessibilityinsights.io/docs/windows/overview) aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les applications Windows. L’outil prend en charge trois scénarios principaux :
  - L' **inspection en direct** permet aux développeurs de vérifier qu’un élément d’une application possède les propriétés UI Automation appropriées simplement en pointant sur l’élément ou en définissant le focus clavier sur celui-ci.
  - **FastPass** : processus léger et en deux étapes qui aide les développeurs à identifier les problèmes d’accessibilité courants et à fort impact en moins de cinq minutes.
  - La **résolution des** problèmes vous permet de diagnostiquer et de corriger des problèmes d’accessibilité spécifiques.

### <a name="legacy-testing-tools"></a>Outils de test hérités

Les outils suivants sont toujours disponibles dans le SDK Windows et sont décrits ici pour une prise en charge continue, mais nous vous recommandons de passer à [Accessibility Insights](https://accessibilityinsights.io/).

- [**Observateur d’événements accessible**](accessible-event-watcher.md): l’outil d’observateur d’événements accessible (AccEvent) examine les données d’accessibilité pour faciliter la validation des éléments d’interface utilisateur de l’application, afin de s’assurer que les éléments de l’interface utilisateur déclenchent des événements Microsoft Active Accessibility et UI Automation appropriés lorsque des modifications d’interface utilisateur se produisent. AccEvent est généralement utilisé pour déboguer les problèmes et pour valider le bon fonctionnement des contrôles personnalisés et étendus.

- [**Inspect**](inspect-objects.md): Inspect vous permet d’afficher les données d’accessibilité dans n’importe quel élément d’interface utilisateur. Elle est particulièrement utile lorsque vous étendez un contrôle commun ou créez un contrôle personnalisé, pour vous assurer que les propriétés et les modèles de contrôle sont correctement définis.

- [**AccScope**](accscope.md): l’outil AccScope permet aux développeurs d’évaluer visuellement l’accessibilité de leur application lors des premières phases de conception et de développement. AccScope permet de visualiser la façon dont un lecteur d’écran utilise les informations UI Automation fournies par une application. Il peut montrer les zones dans lesquelles l’ajout d’informations ou la prise en charge de votre application peut améliorer son accessibilité.

- [**Vérificateur d’accessibilité de l’interface utilisateur**](ui-accessibility-checker.md): l’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker) vérifie que les exigences d’accessibilité de l’interface utilisateur sont respectées. AccChecker comprend des vérifications de vérification pour UI Automation, Microsoft Active Accessibility et des applications Internet riches accessibles (ARIA). Il peut fournir une vérification statique en recherchant des erreurs telles que des noms manquants, des problèmes d’arborescence, etc. Il permet de vérifier l’accès par programme et dispose de fonctionnalités avancées pour prendre en charge l’automatisation des tests d’accessibilité.

- [**Vérification d’UI Automation**](ui-automation-verify.md): vérification d’UI Automation (UIA Verify) est un Framework de test pour les tests manuels et automatisés de l’implémentation d’UI Automation d’un contrôle ou d’une application. Il peut également consigner les résultats des tests. Vous pouvez intégrer votre application dans le code de test et procéder à des tests réguliers, automatisés ou à des contrôles ponctuels de vos scénarios d’automatisation d’interface utilisateur. Cet outil est utile pour vérifier que les modifications apportées aux applications avec des fonctionnalités établies n’ont pas de nouveaux problèmes ou des régressions dans des domaines autres que les nouvelles fonctionnalités.

### <a name="obsolete-tools"></a>Outils obsolètes

L' **Explorateur accessible** et les outils **Spy UI** sont obsolètes et ne sont plus disponibles. Utilisez à la place [**Inspect**](inspect-objects.md) ou [**AccScope**](accscope.md) .

## <a name="related-topics"></a>Rubriques connexes

- [Hub de développeur d’accessibilité](https://developer.microsoft.com/windows/accessible-apps)
- [Accessibilité Microsoft](https://www.microsoft.com/accessibility/)