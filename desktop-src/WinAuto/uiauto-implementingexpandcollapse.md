---
title: Modèle de contrôle ExpandCollapse
description: Fournit des instructions et des conventions pour l’implémentation de IExpandCollapseProvider, y compris des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- UI Automation, implémentation du modèle de contrôle ExpandCollapse
- UI Automation, modèle de contrôle ExpandCollapse
- UI Automation, IExpandCollapseProvider
- IExpandCollapseProvider
- implémentation des modèles de contrôle ExpandCollapse d’UI Automation
- Modèles de contrôle ExpandCollapse
- modèles de contrôle, IExpandCollapseProvider
- modèles de contrôle, implémenter des ExpandCollapse UI Automation
- modèles de contrôle, ExpandCollapse
- interfaces, IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028974"
---
# <a name="expandcollapse-control-pattern"></a>Modèle de contrôle ExpandCollapse

Fournit des instructions et des conventions pour l’implémentation de [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle **ExpandCollapse** est utilisé pour prendre en charge les contrôles qui se développent visuellement pour afficher davantage de contenu et réduire pour masquer le contenu.

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **ExpandCollapse** , notez les conventions et recommandations suivantes :

-   Les contrôles d’agrégat, générés avec des objets enfants qui fournissent l’interface utilisateur avec des fonctionnalités de développement/réduction, doivent prendre en charge le modèle de contrôle **ExpandCollapse** , contrairement à leurs éléments enfants. Par exemple, un contrôle de zone de liste déroulante est généré avec une combinaison de contrôles de zone de liste, de bouton et d’édition, mais seule la zone de liste déroulante parente doit prendre en charge le modèle de contrôle **ExpandCollapse** .
    > [!Note]  
    > Une exception est le contrôle Menu, qui est un agrégat d’objets d’élément de menu individuels. Les objets d’élément de menu peuvent prendre en charge le modèle de contrôle **ExpandCollapse** , mais le contrôle menu parent ne le peut pas. Une exception similaire s’applique aux contrôles d’arborescence et d’élément d’arborescence.

     

-   Lorsque [**IExpandCollapseProvider :: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) d’un contrôle a la valeur **ExpandCollapseState \_ leafnode**, toute fonctionnalité **ExpandCollapse** est actuellement inactive pour le contrôle et la seule information qui peut être obtenue à l’aide de ce modèle de contrôle est la **ExpandCollapseState**. Si des objets enfants sont ajoutés par la suite, les modifications apportées à **ExpandCollapseState** et à la fonctionnalité **ExpandCollapse** sont activées.
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) fait référence uniquement à la visibilité des objets enfants immédiats ; elle ne fait pas référence à la visibilité de tous les objets descendants.
-   Les fonctionnalités [**IExpandCollapseProvider :: Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) et [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) sont spécifiques au contrôle. Voici des exemples de ce comportement.
    -   Le menu personnel d’Office peut être un élément de menu à trois États (« développé », « réduit » et « PartiallyExpanded ») où le contrôle spécifie l’État à adopter quand l’option [**développer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**réduire**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) est appelée.
    -   L’appel de [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) sur un élément d’arborescence peut afficher tous les descendants ou seulement les enfants immédiats.
    -   Si l’appel de [**expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) sur un contrôle conserve l’état de ses descendants, un événement de modification de visibilité doit être envoyé, et non un événement de changement d’État. Si le contrôle parent ne conserve pas l’état de ses descendants lorsqu’il est réduit, le contrôle peut détruire tous les descendants qui ne sont plus visibles et déclencher un événement détruit ; elle peut également modifier les [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) pour chaque descendant et déclencher un événement de modification de visibilité.
-   Pour garantir la navigation, il est souhaitable qu’un objet se trouve dans l’arborescence Microsoft UI Automation (avec un état de visibilité approprié), quel que soit le [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)de ses parents. Si des descendants sont générés à la demande, ils peuvent uniquement apparaître dans l’arborescence UI Automation après avoir été affichés pour la première fois ou uniquement lorsqu’ils sont visibles.

## <a name="required-members-for-iexpandcollapseprovider"></a>Membres requis pour **IExpandCollapseProvider**

Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) .



| Membres nécessaires                                                                                    | Type de membre | Notes                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Propriété    | Aucun                                                                   |
| [**Développez**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Méthode      | Aucun                                                                   |
| [**Réduire**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Méthode      | Aucun                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Événement       | Ce contrôle n’a pas d’événements associés ; Utilisez ce gestionnaire d’événements générique. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




