---
title: Modifier le type de contrôle
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Edit.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- UI Automation, prise en charge du type de contrôle Edit
- UI Automation, modifier le type de contrôle
- UI Automation, arborescence pour le type de contrôle Edit
- UI Automation, propriétés pour le type de contrôle Edit
- UI Automation, modèles de contrôle pour le type de contrôle Edit
- UI Automation, événements pour le type de contrôle d’édition
- arborescences, modifier le type de contrôle
- Propriétés, modifier le type de contrôle
- modèles de contrôle, modifier le type de contrôle
- événements, modifier le type de contrôle
- prise en charge du type de contrôle Edit
- Edit (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Edit
- types de contrôles, modèles de contrôle pour le type de contrôle Edit
- types de contrôles, prise en charge pour la modification
- types de contrôles, modifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122586"
---
# <a name="edit-control-type"></a>Modifier le type de contrôle

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Edit** .

Les contrôles Edit permettent à un utilisateur d’afficher et modifier une simple ligne de texte sans une prise en charge évoluée de la mise en forme.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle Edit. Les exigences d’UI Automation s’appliquent à tous les contrôles d’édition où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’édition et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Modifier</li></ul> | <ul><li>Modifier</li></ul> | 




 

Les contrôles qui implémentent le type de contrôle **Edit** auront toujours des barres de défilement zéro dans l’affichage de contrôle de l’arborescence UI Automation, car il s’agit d’un contrôle à ligne unique. Dans certains scénarios de disposition, la ligne de texte unique peut faire l’objet d’un retour automatique à la ligne. Le type de contrôle **Edit** est conçu uniquement pour les petites quantités de texte.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles d’édition. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Le contrôle d’édition doit avoir un point interactif qui donne le focus d’entrée à la partie d’édition du contrôle quand un utilisateur clique dessus avec la souris.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Modifier**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle d’édition est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle d’édition est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Consultez les remarques. | Doit avoir la valeur **true** pour les contrôles d’édition qui contiennent des mots de passe. Si un contrôle d’édition contient du contenu de mot de passe, cette propriété peut être utilisée par un lecteur d’écran pour déterminer si les séquences de touches doivent être lues au moment où l’utilisateur les tape.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Si une étiquette de texte statique est associée au contrôle, cette propriété doit exposer une référence à ce contrôle. Si le contrôle de texte est un sous-composant d’un autre contrôle, il n’aura pas de propriété **LabeledBy** définie.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Edit** . La valeur par défaut est « modifier » pour en-US ou anglais (États-Unis).                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le nom du contrôle d’édition est habituellement généré à partir d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, une valeur de propriété pour le **nom** doit être affectée par le développeur de l’application. La propriété **Name** ne doit jamais contenir le contenu textuel du contrôle d’édition. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles d’édition. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                              | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dépend       | Tous les contrôles d’édition qui prennent une plage numérique doivent exposer le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) .                                                                                                                                                                                                                                                                                       |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Consultez les remarques.    | Cette propriété doit être la plus petite valeur à laquelle le contenu du contrôle d’édition peut être défini.                                                                                                                                                                                                                                                                                                                     |
| [**Maximale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Consultez les remarques.    | Cette propriété doit être la plus grande valeur à laquelle le contenu du contrôle d’édition peut être défini.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Consultez les remarques.    | Cette propriété doit indiquer le nombre de décimales pouvant être défini pour la valeur. Si le contrôle d’édition accepte uniquement des entiers, la valeur de la propriété **SmallChange** doit être 1. Si le contrôle d’édition prend une plage comprise entre 1,0 et 2,0, la valeur de la propriété **SmallChange** doit être 0,1. Si le contrôle d’édition prend une plage comprise entre 1,00 et 2,00, la valeur de la propriété **SmallChange** doit être 0,001.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Cette propriété n’est pas tenue d’être exposée sur un contrôle d’édition.                                                                                                                                                                                                                                                                                                                                                      |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Consultez les remarques.    | Cette propriété indique le contenu numérique du contrôle d’édition. Quand une valeur plus précise est définie par un client UI Automation dans les plages spécifiées dans les propriétés [**minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) et [**maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) , la propriété [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) est automatiquement arrondie à la valeur acceptée la plus proche. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obligatoire      | Tous les contrôles d’édition doivent prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , car les informations détaillées doivent toujours être disponibles pour les clients de technologie d’assistance.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dépend       | Tous les contrôles d’édition qui prennent une chaîne doivent exposer le modèle de contrôle [value](uiauto-implementingvalue.md) .                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Consultez les remarques.    | Cette propriété doit être définie pour indiquer si le contrôle peut avoir une valeur définie par programme ou qui peut être modifiée par l’utilisateur.                                                                                                                                                                                                                                                                                |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Consultez les remarques.    | Cette propriété contient le contenu textuel du contrôle d’édition. Si la propriété [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) a la valeur **true**, l’interrogation de la propriété [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) doit retourner une erreur.                                                                                                                      |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’édition. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                                                |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.                             | Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Un contrôle d’édition ne prend jamais en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                                      | Si le contrôle prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , il doit prendre en charge cet événement.   |
| [**\_TextSelectionChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                      | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="remarks"></a>Notes

Un contrôle d’édition peut être utilisé en tant que champ de texte en lecture seule qui ne prend pas en charge la sélection ou la modification de texte. Un tel contrôle d’édition se comporte comme un objet de champ qui a un nom et une valeur spécifiques.

Si un contrôle d’édition contient du texte d’espace réservé (par exemple, une bannière de signalement), le texte doit être utilisé comme propriété **HelpText** , sauf si le texte peut être modifié par l’utilisateur, puis réutilisé comme texte d’espace réservé. par exemple, le Windows barre d’adresses d’Internet Explorer contient le texte « about : Tabs » lorsqu’un nouvel onglet est ouvert. Il ne s’agit pas de **HelpText** , car il s’agit d’une adresse de programmation qui peut être utilisée ou modifiée par l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




