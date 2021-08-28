---
title: Type de contrôle SemanticZoom
description: Cette rubrique fournit des informations sur la prise en charge d’UI Automation pour le type de contrôle SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- UI Automation, prise en charge du type de contrôle SemanticZoom
- UI Automation, type de contrôle SemanticZoom
- UI Automation, arborescence pour le type de contrôle SemanticZoom
- UI Automation, propriétés du type de contrôle SemanticZoom
- UI Automation, modèles de contrôle pour le type de contrôle SemanticZoom
- UI Automation, événements pour le type de contrôle SemanticZoom
- arborescences, type de contrôle SemanticZoom
- Propriétés, type de contrôle SemanticZoom
- modèles de contrôle, type de contrôle SemanticZoom
- événements, type de contrôle SemanticZoom
- prise en charge du type de contrôle SemanticZoom
- Type de contrôle SemanticZoom
- types de contrôles, arborescence pour le type de contrôle SemanticZoom
- types de contrôle, modèles de contrôle pour le type de contrôle SemanticZoom
- types de contrôle, prise en charge de SemanticZoom
- types de contrôles, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9673c5e9beb0c78ecc7dfccc10b6716d6d3afa3f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467756"
---
# <a name="semanticzoom-control-type"></a>Type de contrôle SemanticZoom

Cette rubrique fournit des informations sur la prise en charge d’UI Automation pour le type de contrôle **SemanticZoom** .

le Zoom sémantique est une technique introduite dans Windows 8 pour la présentation et la navigation dans de grands ensembles de données ou de contenu connexes dans une seule vue, par exemple un album photo, une liste d’applications ou un carnet d’adresses. Le zoom sémantique utilise deux modes distincts de classification, ou *niveaux de zoom*, pour l’organisation et la présentation du contenu. Le mode de bas niveau (ou *Zoom avant*) affiche les éléments dans une structure « tout-en-un » plat. et le mode de haut niveau (ou *Zoom arrière*) affiche des éléments dans des groupes, ce qui permet à l’utilisateur de parcourir rapidement le contenu. Par exemple, le zoom d’une liste de villes peut passer à une liste d’États contenant ces villes. Le zoom d’une liste de programmes peut être modifié en une liste de groupes de programmes logiques.

pour plus d’informations sur le zoom sémantique spécifiquement utilisé pour les applications Windows store, consultez [instructions pour le zoom sémantique](/windows/uwp/controls-and-patterns/semantic-zoom).

Le modèle d’utilisation pour le type de contrôle **SemanticZoom** est inhabituel, car il existe principalement pour l’accès par programme. Les clients UI Automation de Microsoft peuvent surveiller et manipuler le contrôle de zoom sémantique pour contrôler l’état de zoom de la liste. Les utilisateurs qui n’utilisent pas la technologie d’assistance manipulent généralement le contrôle de zoom sémantique directement par le biais de gestes tactiles ou de raccourcis clavier.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **SemanticZoom** . Les spécifications d’UI Automation s’appliquent à tous les contrôles de zoom sémantique où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle et propriétés obligatoires](#required-control-patterns-and-properties)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation qui se rapporte au type de contrôle **SemanticZoom** et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>List<ul><li>SemanticZoom<ul><li>ListItem (0 ou plus)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>ListItem (0 ou plus)</li></ul></li></ul> | 




 

Ou :




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>SemanticZoom<ul><li>List<ul><li>ListItem (0 ou plus)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>ListItem (0 ou plus)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **SemanticZoom** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).




| Propriété UI Automation | Valeur | Notes | 
|------------------------|-------|-------|
| <a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a> | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a> | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a> | Consultez les remarques. | Si le contrôle de liste a un point interactif (point sur lequel vous pouvez cliquer pour que la liste prenne le focus), ce point doit être exposé via cette propriété. Si la valeur de la propriété <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> a la valeur <strong>true</strong>, la tentative d’extraction de cette propriété entraîne l’erreur <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> . | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a> | <strong>SemanticZoom</strong> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a> | FALSE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a> | Consultez les remarques. | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a> | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle <strong>SemanticZoom</strong> . La valeur par défaut est « zoom sémantique » pour « fr-fr » ou « anglais » (États-Unis).<blockquote>[!Note]<br />Certaines infrastructures ont concaténées comme « semanticzoom ».</blockquote><br /> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a> | Consultez les remarques. | Une chaîne vide est acceptable, ou un nom plus utile peut être fourni, à condition qu’elle ne contienne pas le terme zoom sémantique, ce qui rendrait la combinaison du type de contrôle et du nom déroutante. | 




 

## <a name="required-control-patterns-and-properties"></a>Modèles de contrôle et propriétés obligatoires

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de zoom sémantique. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                  | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Dépend       | Les contrôles de zoom sémantique prennent en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) pour permettre l’activation ou la désactivation du zoom. [**ToggleState \_ OFF**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) correspond à l’État Flat, All-up, et [**ToggleState \_ on**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) correspond à la vue de niveau supérieur, zoom arrière. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de zoom sémantique. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="remarks"></a>Remarques

Si une interface utilisateur a un bouton visible pour activer/désactiver le comportement du contrôle de zoom sémantique, ce bouton ne doit pas avoir de type de contrôle **SemanticZoom** . Il s’agit d’un compteur intuitif, mais le type de contrôle **SemanticZoom** caractérise le conteneur du contenu de zoom, pas un bouton qui contrôle le zoom. (Un bouton peut être représenté simplement sous la forme d’un type de contrôle [Button](uiauto-supportbuttoncontroltype.md) avec le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) .)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

