---
title: Architecture et interopérabilité
description: Cette rubrique décrit brièvement l’architecture de Microsoft Active Accessibility et Microsoft UI Automation, ainsi que les composants qui permettent l’interopérabilité entre les applications basées sur les deux technologies différentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104101185"
---
# <a name="architecture-and-interoperability"></a>Architecture et interopérabilité

Cette rubrique décrit brièvement l’architecture de Microsoft Active Accessibility et Microsoft UI Automation, ainsi que les composants qui permettent l’interopérabilité entre les applications basées sur les deux technologies différentes.

Pour plus d’informations sur l’interopérabilité entre Microsoft Active Accessibility et UI Automation, consultez [infrastructure commune](common-infrastructure.md).

Cette rubrique contient les sections suivantes.

-   [Architecture de Microsoft Active Accessibility](#microsoft-active-accessibility-architecture)
-   [Architecture d’UI Automation](#ui-automation-architecture)
-   [Interopérabilité entre Microsoft Active Accessibility et UI Automation](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Interface IAccessibleEx](#the-iaccessibleex-interface)
-   [Rubriques connexes](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Architecture de Microsoft Active Accessibility

Microsoft Active Accessibility expose des informations de base sur les contrôles tels que le nom du contrôle, l’emplacement à l’écran et le type de contrôle, ainsi que des informations d’État telles que la visibilité et l’état activé/désactivé. L’interface utilisateur est représentée sous la forme d’une hiérarchie d’objets accessibles. les modifications et les actions sont représentées en tant que WinEvents.

Microsoft Active Accessibility comprend les composants suivants :

-   Objet accessible : élément d’interface utilisateur logique (tel qu’un bouton) qui est représenté par une interface COM (Component Object Model) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un identificateur enfant entier (childID).
-   WinEvents : système d’événements qui permet aux serveurs de notifier les clients lorsqu’un objet accessible change. Pour plus d’informations, consultez [winEvents](winevents-infrastructure.md).
-   OLEACC.dll : la bibliothèque de liens dynamiques au moment de l’exécution qui fournit l’API Microsoft Active Accessibility et l’infrastructure du système d’accessibilité. OLEACC implémente les objets proxy qui fournissent des informations d’accessibilité par défaut pour les éléments d’interface utilisateur standard, y compris les contrôles utilisateur, les menus utilisateur et les contrôles communs.

Pour Microsoft Active Accessibility, le composant système de l’infrastructure d’accessibilité (OLEACC) permet la communication entre les technologies d’assistance (outils d’accessibilité) et les applications, comme le montre l’illustration suivante.

![Illustration montrant comment les outils d’accessibilité interagissent avec les applications](images/msaaarch.gif)

Les applications (serveurs Microsoft Active Accessibility) fournissent des informations d’accessibilité de l’interface utilisateur aux outils (clients Microsoft Active Accessibility), qui interagissent avec l’interface utilisateur pour le compte des utilisateurs. La limite de code est à la fois une limite de programmation et de processus.

## <a name="ui-automation-architecture"></a>Architecture d’UI Automation

Avec UI Automation, le composant principal d’UI Automation (UIAutomationCore.dll) est chargé à la fois dans les processus des outils d’accessibilité et des applications. Le composant principal gère la communication entre processus, fournit des services de niveau supérieur tels que la recherche d’éléments par valeurs de propriété, et active l’extraction ou la mise en cache en bloc des propriétés, ce qui offre de meilleures performances que l’implémentation de Microsoft Active Accessibility.

UI Automation comprend des objets proxy qui fournissent des informations sur l’interface utilisateur sur les éléments d’interface utilisateur standard, tels que les contrôles utilisateur, les menus utilisateur et les contrôles communs. Il comprend également des proxies qui permettent aux clients UI Automation d’accéder aux informations de l’interface utilisateur auprès des serveurs Microsoft Active Accessibility.

L’illustration suivante montre les relations entre les différents compontents d’automatisation d’interface utilisateur utilisés dans les outils d’accessibilité (clients) et dans les applications (fournisseurs).

![Illustration montrant comment les composants des outils d’accessibilité interagissent avec ceux des applications](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Interopérabilité entre Microsoft Active Accessibility et UI Automation

L’automatisation de l’interface utilisateur de Microsoft Active Accessibility Bridge permet aux clients Microsoft Active Accessibility d’accéder aux fournisseurs UI Automation en convertissant le modèle objet UI Automation en modèle objet Microsoft Active Accessibility. L’illustration suivante montre le rôle du pont UI Automation-à-Microsoft Active Accessibility.

![illustration illustrant le fonctionnement d’UI Automation avec les outils et applications d’accessibilité](images/uiatomsaabridge.gif)

De même, le proxy d’automatisation Microsoft Active Accessibility-to-UI traduit les modèles d’objet serveur basés sur Microsoft Active Accessibility pour les clients UI Automation. L’illustration suivante montre le rôle du proxy Automation de Microsoft Active Accessibility à UI.

![illustration illustrant le fonctionnement du proxy UI Automation avec les outils et applications d’accessibilité](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>Interface IAccessibleEx

L’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permet aux applications ou bibliothèques d’interface utilisateur existantes d’étendre leur modèle objet Microsoft Active Accessibility pour prendre en charge l’Automation d’interface utilisateur sans réécrire l’implémentation de zéro. Avec **IAccessibleEx**, vous pouvez implémenter uniquement les propriétés UI Automation supplémentaires et les modèles de contrôle nécessaires pour décrire entièrement l’interface utilisateur et ses fonctionnalités.

Étant donné que le proxy Automation de Microsoft Active Accessibility à l’interface utilisateur traduit les modèles objet des serveurs Microsoft Active Accessibility compatibles avec [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)en tant que modèles objet UI Automation, les clients UI Automation n’ont pas besoin d’effectuer d’autres tâches. L’interface **IAccessibleEx** peut également permettre aux clients Microsoft Active Accessibilitys in-process d’interagir directement avec les fournisseurs UI Automation.

Pour plus d’informations, consultez [l’interface IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de l’API Windows Automation](windows-automation-api-overview.md)
</dt> <dt>

[Interface IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Considérations relatives à la sécurité pour les technologies d’assistance](uiauto-securityoverview.md)
</dt> </dl>

 

 




