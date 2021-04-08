---
title: Vue d’ensemble de l’arborescence UI Automation
description: Les produits de technologie d’assistance et les scripts de test parcourent l’arborescence Microsoft UI Automation pour recueillir des informations sur l’interface utilisateur et ses éléments.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- UI Automation, vue d’ensemble de l’arborescence
- UI Automation, vue de l’arborescence
- UI Automation, vue brute de l’arborescence
- UI Automation, affichage des contrôles de l’arborescence
- UI Automation, affichage du contenu de l’arborescence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839822"
---
# <a name="ui-automation-tree-overview"></a>Vue d’ensemble de l’arborescence UI Automation

Les produits de technologie d’assistance et les scripts de test parcourent l’arborescence Microsoft UI Automation pour recueillir des informations sur l’interface utilisateur et ses éléments.

L’arborescence UI Automation est un élément racine qui représente la fenêtre du bureau Windows (« le bureau ») et dont les éléments enfants représentent des fenêtres d’application. Chacun de ces éléments enfants peut contenir des éléments qui représentent des éléments de l’interface utilisateur, tels que des menus, des boutons, des barres d’outils et des zones de liste. Ces éléments peuvent contenir des éléments, tels que des éléments de liste.

L’arborescence UI Automation n’est pas une structure fixe. Elle est rarement perçue dans son total, car elle peut contenir des milliers d’éléments. Les parties de l’arborescence UI Automation sont générées lorsqu’un client en a besoin, et la structure de l’arborescence change à mesure que des éléments sont ajoutés, déplacés ou supprimés.

Les fournisseurs UI Automation prennent en charge l’arborescence UI Automation en implémentant la navigation entre les éléments d’un fragment. Un fragment est une sous-arborescence complète d’éléments d’une infrastructure particulière et a un élément racine (appelé *racine de fragment*) qui est généralement hébergé dans une fenêtre.

Les fournisseurs ne sont pas concernés par la navigation d’un contrôle à un autre. Cela est géré par le noyau UI Automation, qui utilise les informations des fournisseurs de fenêtres par défaut.

Cette rubrique contient les sections suivantes.

-   [Affichages de l’arborescence UI Automation](#views-of-the-ui-automation-tree)
    -   [Affichage brut](#raw-view)
    -   [Vue de contrôle](#control-view)
    -   [Affichage du contenu](#content-view)
-   [Rubriques connexes](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Affichages de l’arborescence UI Automation

L’arborescence UI Automation peut être filtrée pour créer des affichages qui contiennent uniquement les éléments UI Automation pertinents pour un client particulier. Cette approche permet aux clients de personnaliser la structure présentée par le biais d’UI Automation en fonction de leurs besoins spécifiques.

Le client peut personnaliser la vue en étendue et en filtrant. La portée définit l’étendue de la vue, à partir d’un élément de base. Par exemple, l’application peut souhaiter Rechercher uniquement les enfants directs du bureau, ou tous les descendants d’une fenêtre d’application. Le filtrage définit les types d’éléments inclus dans la vue.

Les fournisseurs UI Automation prennent en charge le filtrage en définissant des propriétés sur les éléments, y compris les propriétés [**IUIAutomationElement :: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) et [**IUIAutomationElement :: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

UI Automation fournit trois vues par défaut : affichage brut, vue de contrôle et affichage du contenu. Ces vues sont définies par le type de filtrage effectué. L’étendue d’une vue est définie par l’application. L’application peut appliquer d’autres filtres sur les propriétés. par exemple, pour inclure uniquement des contrôles activés dans une vue de contrôle.

### <a name="raw-view"></a>Affichage brut

L’affichage brut de l’arborescence UI Automation est l’arborescence complète des éléments Automation pour lesquels le bureau est la racine. L’affichage brut suit étroitement la structure de programmation native d’une application et est la vue la plus détaillée disponible. C’est aussi la base sur laquelle reposent les autres affichages de l’arborescence. Étant donné que cette vue dépend de l’infrastructure d’interface utilisateur sous-jacente, l’affichage brut d’un bouton Windows Presentation Foundation (WPF) a une vue brute différente de celle d’un bouton Microsoft Win32.

La vue brute est obtenue en recherchant des éléments sans spécifier de propriétés ou à l’aide de [**IUIAutomation :: RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) pour obtenir une interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) pour naviguer dans l’arborescence.

### <a name="control-view"></a>Affichage de contrôle

L’affichage de contrôle est un sous-ensemble de l’affichage brut. Il comprend uniquement les éléments d’interface utilisateur dont la propriété [**IUIAutomationElement :: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) a la valeur **true**.

L’affichage de contrôle comprend les éléments d’interface utilisateur qui fournissent des informations à l’utilisateur ou qui permettent à l’utilisateur d’effectuer une action. Il s’agit des éléments d’interface utilisateur les plus intéressants pour les applications de tests automatisés.

L’affichage de contrôle comprend également des éléments d’interface utilisateur non interactifs qui contribuent à la structure logique de l’interface utilisateur. Celles-ci incluent des conteneurs d’éléments tels que les en-têtes de vue de liste, les barres d’outils, les menus et la barre d’État. Les autres éléments non interactifs qui apparaissent dans l’affichage de contrôle sont des graphiques avec des informations et du texte statique dans une boîte de dialogue.

Les éléments non interactifs utilisés uniquement à des fins de disposition ou décoratives, tels que les panneaux utilisés pour disposer les contrôles dans une boîte de dialogue, n’apparaissent pas dans l’affichage de contrôle.

L’affichage de contrôle de l’arborescence UI Automation correspond étroitement à la structure d’interface utilisateur perçue par un utilisateur final. Cela permet au produit de technologie d’assistance de décrire plus facilement l’interface utilisateur à l’utilisateur final et d’aider l’utilisateur final à interagir avec l’application.

L’affichage de contrôle est obtenu en recherchant des éléments dont la propriété [**IUIAutomationElement :: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) a la valeur true, ou en utilisant [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) pour obtenir une interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) pour naviguer dans l’arborescence.

### <a name="content-view"></a>Affichage de contenu

L’affichage de contenu de l’arborescence UI Automation est un sous-ensemble de l’affichage de contrôle. Il comprend uniquement les éléments d’interface utilisateur dont la propriété [**IUIAutomationElement :: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) et la propriété [**IUIAutomationElement :: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) ont la valeur **true**.

L’affichage de contenu contient des éléments d’interface utilisateur qui communiquent les informations réelles dans une interface utilisateur, y compris les éléments d’interface utilisateur qui peuvent recevoir le focus clavier et du texte qui n’est pas une étiquette sur un élément d’interface utilisateur. Il s’agit des éléments d’interface utilisateur les plus intéressants pour une application de lecteur d’écran. Par exemple, les valeurs d’une zone de liste déroulante déroulante s’affichent dans l’affichage du contenu, car les valeurs représentent les informations utilisées par un utilisateur final.

Dans l’affichage de contenu, une zone de liste déroulante et une zone de liste sont toutes deux représentées sous la forme d’un ensemble d’éléments d’interface utilisateur dans lesquels un ou plusieurs éléments peuvent être sélectionnés. Le fait qu’un élément soit toujours ouvert et un élément peut être développé et réduit n’est pas pertinent dans l’affichage du contenu, car il est conçu pour afficher les données, ou le contenu, qui sont présentées à l’utilisateur.

L’affichage du contenu est obtenu en recherchant des éléments dont la propriété [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) et [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) a la valeur **true**, ou à l’aide de [**IUIAutomation :: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) pour obtenir une interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) pour naviguer dans l’arborescence.

Les images suivantes montrent les différences entre l’affichage de contrôle et l’affichage de contenu. La première image montre une zone de liste modifiable simple avec trois éléments dans la liste déroulante. La deuxième image montre comment les éléments d’interface utilisateur de la zone de liste déroulante apparaissent dans les affichages de contrôle et de contenu de l’application UISpy.exe.

![capture d’écran d’une zone de liste modifiable simple avec trois éléments déroulants](images/combobox.png)

![capture d’écran de l’application UISpy avec affichages de contrôle et de contenu des éléments de zone de liste déroulante](images/treeviews.jpg)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Création de l’objet CUIAutomation](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Obtention d'éléments UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Notions de base d’UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 




