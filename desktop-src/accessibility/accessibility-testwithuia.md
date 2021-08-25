---
description: Vue d’ensemble de l’utilisation d’UI Automation et d’autres outils pour tester vos applications.
title: Tests d’accessibilité
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0cc1d118c84e2689b6cf329da29bb518a566fb8588c311229be17fcd28825ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896579"
---
# <a name="testing-for-accessibility"></a>Tests d’accessibilité

L’accès par programme et l’accès au clavier sont des exigences critiques pour la prise en charge de l’accessibilité dans votre application. le test de l’accessibilité de vos applications Windows, des outils de technologie d’assistance (AT) et des frameworks d’interface utilisateur est essentiel pour garantir une expérience utilisateur réussie pour les personnes ayant des handicaps et des limitations variés (notamment la vision, l’apprentissage, la dextérité et la mobilité et les handicaps de langue/communication), ou ceux qui préfèrent simplement utiliser un clavier.

Sans un accès adéquat via, par exemple, les lecteurs d’écran et les claviers à l’écran, les utilisateurs disposant de troubles de la vision, de l’apprentissage, de la mobilité et de la langue/communication, ainsi que les limitations (et les utilisateurs qui préfèrent utiliser le clavier) ne peuvent pas utiliser votre application.

cette section décrit les différents outils qui peuvent être utilisés pour tester l’implémentation de l’accessibilité des applications Windows et web.

> [!NOTE]
> Il est également important d’effectuer des tests manuels pour vérifier l’accès au clavier à votre application.

## <a name="tools"></a>Outils

[accessibilité Informations](https://accessibilityinsights.io/) : aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les applications web et Windows.

- l' [accessibilité Informations pour le Web](https://accessibilityinsights.io/docs/web/overview) est une extension pour Chrome et [Microsoft Edge insider](https://www.microsoftedgeinsider.com) qui aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les sites et les applications Web. Il prend en charge deux scénarios principaux :
  - **FastPass** : processus léger et en deux étapes qui aide les développeurs à identifier les problèmes d’accessibilité courants et à fort impact en moins de cinq minutes.  
  - **Évaluation** : permet à quiconque de vérifier qu’un site Web est compatible 100% avec les normes et les consignes d’accessibilité. l' [accessibilité Informations](https://accessibilityinsights.io/) vous permet également de consulter les éléments, les propriétés, les modèles de contrôle et les événements UI Automation (comme les outils hérités [inspecter](/windows/desktop/winauto/inspect-objects) et [AccEvent](/windows/desktop/winauto/accessible-event-watcher) décrits dans la section suivante).

- l' [accessibilité Informations pour Windows](https://accessibilityinsights.io/docs/windows/overview) aide les développeurs à trouver et à résoudre les problèmes d’accessibilité dans les applications Windows. L’outil prend en charge trois scénarios principaux :
  - L' **inspection en direct** permet aux développeurs de vérifier qu’un élément d’une application possède les propriétés UI Automation appropriées simplement en pointant sur l’élément ou en définissant le focus clavier sur celui-ci.
  - **FastPass** : processus léger et en deux étapes qui aide les développeurs à identifier les problèmes d’accessibilité courants et à fort impact en moins de cinq minutes.
  - La **résolution des** problèmes vous permet de diagnostiquer et de corriger des problèmes d’accessibilité spécifiques.

### <a name="legacy-testing-tools"></a>Outils de test hérités

les outils suivants sont toujours disponibles dans le SDK Windows et sont décrits ici pour une prise en charge continue, mais nous vous recommandons de passer à l' [accessibilité Informations](https://accessibilityinsights.io/).

- [Inspect](/windows/desktop/winauto/inspect-objects): vous permet d’afficher les données d’accessibilité de n’importe quel élément d’interface utilisateur. Elle est particulièrement utile pour s’assurer que les propriétés et les modèles de contrôle sont correctement définis lors de l’extension d’un contrôle commun ou de la création d’un contrôle personnalisé.
- [Observateur d’événements accessible (AccEvent)](/windows/desktop/winauto/accessible-event-watcher): examine les données d’accessibilité pour valider les éléments d’interface utilisateur de l’application et vérifier que les éléments de l’interface utilisateur déclenchent les événements Microsoft Active Accessibility et UI Automation appropriés sur les événements d’interface utilisateur. AccEvent est généralement utilisé pour déboguer les problèmes et pour valider le bon fonctionnement des contrôles personnalisés et étendus.
- [AccScope](/windows/desktop/winauto/accscope): active l’évaluation visuelle de l’accessibilité d’une application lors des premières phases de conception et de développement. AccScope permet de visualiser la façon dont un lecteur d’écran utilise les informations UI Automation fournies par une application, et indique où l’ajout d’informations ou la prise en charge de votre application peut améliorer son accessibilité.
- [Outil d’analyse de l’accessibilité de l’interface utilisateur](/windows/desktop/winauto/ui-accessibility-checker): vérifie que les exigences d’accessibilité clés dans une application sont atteintes. AccChecker comprend des vérifications de vérification pour UI Automation, Microsoft Active Accessibility et des applications Internet riches accessibles (ARIA). Il peut fournir une vérification statique des erreurs telles que les noms manquants, les problèmes d’arborescence et bien plus encore. Il permet de vérifier l’accès par programme et comprend des fonctionnalités avancées pour l’automatisation des tests d’accessibilité.
- [Vérification d’UI Automation](/windows/desktop/winauto/ui-automation-verify): infrastructure pour les tests manuels et automatisés de l’implémentation d’UI Automation dans un contrôle ou une application (les résultats peuvent être journalisés). Vous pouvez intégrer votre application dans le code de test et procéder à des tests réguliers, automatisés ou à des contrôles ponctuels de vos scénarios d’automatisation d’interface utilisateur. Cet outil est utile pour vérifier que les modifications apportées aux applications avec des fonctionnalités établies n’ont pas de nouveaux problèmes ou des régressions dans des domaines autres que les nouvelles fonctionnalités.
