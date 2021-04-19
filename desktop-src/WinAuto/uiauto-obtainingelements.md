---
title: Obtention d'éléments UI Automation
description: Cette rubrique décrit les différentes façons d’obtenir des interfaces IUIAutomationElement pour les éléments d’interface utilisateur.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- clients, obtention d’éléments UI Automation
- clients, éléments UI Automation
- clients, éléments racines
- clients, étendue de la recherche
- UI Automation, obtenir des éléments
- UI Automation, éléments
- UI Automation, éléments racine
- UI Automation, conditions
- UI Automation, zone de recherche
- obtention d’éléments UI Automation
- éléments racines
- étendue de recherche
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: a1adbcea5cea81f97350ef15c491b289e07d3ee6
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106539487"
---
# <a name="obtaining-ui-automation-elements"></a>Obtention d'éléments UI Automation

Cette rubrique décrit les différentes façons d’obtenir des interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour les éléments d’interface utilisateur.

**IUIAutomationElement** est utilisé dans l' [exemple d’application cliente de contenu de document UI Automation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient).

## <a name="root-element"></a>Élément racine

Bien que les éléments puissent être récupérés directement à l’aide de méthodes, telles que [**IUIAutomation :: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), certaines applications clientes requièrent une vue de la structure hiérarchique des éléments, appelée arborescence UI Automation. L’élément racine de cette hiérarchie est le bureau. Vous pouvez obtenir cet élément à l’aide de la méthode [**IUIAutomation :: GetRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) ou de la méthode [**IUIAutomation :: GetRootElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) . Ces deux méthodes récupèrent un pointeur d’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Vous pouvez rechercher des éléments descendants à l’aide de méthodes, telles que [**IUIAutomationElement :: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) et [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> En général, vous devez essayer d’obtenir uniquement les enfants directs de l’élément racine. Une recherche de descendants peut itérer au sein de centaines ou de milliers d’éléments. Si vous tentez d’obtenir un élément spécifique de niveau inférieur, vous devez commencer votre recherche à partir de la fenêtre d’application ou d’un conteneur de niveau inférieur.

 

## <a name="conditions"></a>Conditions

Pour la plupart des techniques que vous utilisez pour récupérer des éléments UI Automation, vous devez spécifier une condition. Une condition est un ensemble de critères définissant les éléments que vous souhaitez récupérer. Une condition est représentée par l’interface [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) .

La condition la plus simple est la vraie condition, qui est un objet prédéfini qui spécifie que tous les éléments de la zone de recherche doivent être retournés. La fausse condition est l’inverse de la condition vraie et est moins utile, car elle empêche la recherche d’éléments. Vous pouvez obtenir une interface pour la vraie condition à l’aide de [**IUIAutomation :: CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Trois autres conditions prédéfinies, disponibles en tant que propriétés sur l’objet [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , peuvent être utilisées seules ou associées à d’autres conditions : [**IUIAutomation :: ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)et [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, utilisé par lui-même, est équivalent à la condition true, car il ne filtre pas les éléments par les propriétés [**IUIAutomationElement :: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) ou [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

D’autres conditions sont générées à partir d’objets condition, chacun d’entre eux spécifiant une valeur de propriété. Par exemple, une condition de propriété peut spécifier que l’élément est activé ou qu’il prend en charge un certain modèle de contrôle.

Les conditions qui utilisent une logique booléenne peuvent être combinées en appelant [**IUIAutomation :: CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**CreateOrCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)et les méthodes associées.

## <a name="search-scope"></a>Étendue de recherche

Les recherches effectuées à l’aide de [**IUIAutomationElement :: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) ou [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) doivent avoir une étendue et un emplacement de départ.

> [!Note]  
> Les commentaires sur ces deux méthodes s’appliquent également à [**IUIAutomationElement :: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) et [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

L’étendue définit l’espace autour de l’emplacement de départ dans lequel effectuer la recherche. Cela peut inclure l’élément lui-même, ses frères, son parent, ses enfants immédiats et ses descendants. N’oubliez pas que les méthodes **Find** ne prennent pas en charge la recherche dans l’arborescence Microsoft UI Automation. autrement dit, la recherche d’éléments ancêtres n’est pas prise en charge.

La portée d’une recherche est définie par une combinaison d’opérations de bits de valeurs à partir du type énuméré [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) .

## <a name="finding-a-known-element"></a>Recherche d’un élément connu

Pour rechercher un élément connu identifié par un nom, un ID Automation ou une autre propriété ou combinaison de propriétés, il est plus facile d’utiliser la méthode [**IUIAutomationElement :: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) . Si l’élément recherché est une fenêtre d’application, le point de départ de la recherche peut être l’élément racine.

Cette façon de rechercher des éléments UI Automation est particulièrement utile dans les scénarios de tests automatisés.

Pour obtenir un exemple de code qui montre comment rechercher un élément connu, consultez [recherche d’un élément par nom](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Recherche d’éléments dans une sous-arborescence

Pour rechercher tous les éléments qui répondent à des critères spécifiques et qui sont liés à un élément connu, vous pouvez appeler [**IUIAutomationElement :: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) sur l’élément connu. Par exemple, utilisez cette méthode pour récupérer des éléments de liste ou des éléments de menu à partir d’une liste ou d’un menu, ou pour identifier tous les contrôles dans une boîte de dialogue.

Pour obtenir un exemple de code qui montre comment rechercher des éléments dans une sous-arborescence, consultez [recherche d’éléments associés](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Parcourir une sous-arborescence

Si vous n’avez aucune connaissance préalable des applications avec lesquelles votre client peut être utilisé, vous pouvez construire une sous-arborescence de tous les éléments d’intérêt à l’aide de [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). Votre client peut effectuer cette opération, par exemple, en réponse à un événement de modification de focus. autrement dit, lorsqu’une application ou un contrôle reçoit le focus d’entrée, le client UI Automation examine les enfants, voire tous les descendants de l’élément ayant le focus.

Sachez que le parcours de l’arborescence UI Automation est gourmand en ressources. Parcourez l’arborescence uniquement lorsqu’il n’est pas possible d’utiliser les méthodes [**IUIAutomationElement :: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)ou [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) .

Vous pouvez définir votre propre Explorateur d’arborescence en passant une condition personnalisée à [**IUIAutomation :: CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker), ou vous pouvez utiliser l’un des objets prédéfinis suivants qui sont définis en tant que propriétés du [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)de base.



| Object                                                              | Objectif                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Recherche uniquement les éléments dont la propriété [**IUIAutomationElement :: CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) a la **valeur true**. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Recherche uniquement les éléments dont la propriété [**IUIAutomationElement :: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) a la **valeur true**. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Recherche tous les éléments.                                                                                                                                          |



 

Après avoir obtenu un [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker), appelez les méthodes **IUIAutomationTreeWalker :: GetXxx** pour naviguer parmi les éléments de la sous-arborescence, en passant l’élément à partir duquel commencer à parcourir.

La méthode [**IUIAutomationTreeWalker :: Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) peut être utilisée pour naviguer vers un élément dans la sous-arborescence à partir d’un autre élément qui ne fait pas partie de la vue. Par exemple, supposons que vous créez une vue d’une sous-arborescence à l’aide de [**IUIAutomation :: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). Votre application reçoit une notification indiquant qu’une barre de défilement a reçu le focus d’entrée. Comme une barre de défilement n’est pas un élément de contenu, elle n’est pas présente dans l’affichage de la sous-arborescence. Toutefois, vous pouvez passer le [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) qui représente la barre de défilement à **IUIAutomationTreeWalker :: Normalize** et récupérer l’ancêtre le plus proche qui se trouve dans l’affichage de contenu.

Pour obtenir des exemples de code qui montrent comment utiliser l’interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) , consultez [Guide pratique pour parcourir l’arborescence UI Automation](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Autres moyens de récupérer un élément

Outre les recherches et la navigation, vous pouvez récupérer un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de l’une des manières suivantes.

### <a name="from-an-event"></a>À partir d’un événement

Lorsque votre application reçoit un événement UI Automation, l’objet source passé à votre gestionnaire d’événements est représenté par un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Par exemple, si vous vous abonnez à des événements de modification du focus, la source passée à votre [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) est l’élément qui a reçu le focus. Pour plus d’informations, consultez [abonnement à des événements UI Automation](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>À partir d’un point

Pour récupérer un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) à partir de coordonnées d’écran, par exemple, une position de curseur, utilisez la méthode [**IUIAutomation :: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) .

### <a name="from-a-window-handle"></a>À partir d’un handle de fenêtre

Pour récupérer un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) à partir d’un **HWND**, utilisez la méthode [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) .

### <a name="from-the-focused-control"></a>À partir du contrôle ayant le focus

Pour récupérer un [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) qui représente le contrôle ayant le focus, utilisez la méthode [**IUIAutomation :: GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) .

## <a name="related-topics"></a>Rubriques connexes

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)

[Exemple d’application de client de contenu de document UI Automation](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
