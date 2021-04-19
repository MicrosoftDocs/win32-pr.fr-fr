---
title: Image (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle image.
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- UI Automation, prise en charge du type de contrôle image
- UI Automation, type de contrôle image
- UI Automation, arborescence pour le type de contrôle image
- UI Automation, propriétés du type de contrôle image
- UI Automation, modèles de contrôle pour le type de contrôle image
- UI Automation, événements pour le type de contrôle image
- arborescences, type de contrôle image
- Propriétés, type de contrôle image
- modèles de contrôle, type de contrôle image
- événements, type de contrôle image
- prise en charge du type de contrôle image
- Image (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle image
- types de contrôle, modèles de contrôle pour le type de contrôle image
- types de contrôles, prise en charge de l’image
- types de contrôles, image
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "106510036"
---
# <a name="image-control-type"></a>Image (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **image** .

Les contrôles d’image utilisés comme icônes, graphiques d’information et graphiques prendront en charge le type de contrôle **image** . Les contrôles utilisés comme images d’arrière-plan ou de filigrane ne prennent pas en charge le type de contrôle **image** .

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **image** . Les exigences d’UI Automation s’appliquent à tous les contrôles d’image où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

- [Structure d’arborescence classique](#typical-tree-structure)
- [Propriétés pertinentes](#relevant-properties)
- [Modèles de contrôle requis](#required-control-patterns)
- [Événements obligatoires](#required-events)
- [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’image et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).

| Vue de contrôle | Vue de contenu |
| ------------ | ------------ |
| Image | Image (selon que l’image contient des informations, en fonction de la valeur de la propriété des [identificateurs de propriété de l’élément Automation](uiauto-automation-element-propids.md) ) |

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles image. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).

| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Le point cliquable du contrôle d’image doit être un point dans le rectangle englobant du contrôle image.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Image**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | La propriété **HelpText** expose une chaîne localisée qui décrit l’apparence visuelle réelle du contrôle ou d’autres informations d’info-bulle associées à l’image. Cette propriété doit être prise en charge lorsqu’une longue Description est nécessaire pour transmettre plus d’informations sur le contrôle image (par exemple, si l’image est un graphique ou un diagramme complexe). Cette propriété correspond à la balise HTML **longdesc** et à la balise SVG (Scalable Vector Graphics) **desc** . Les développeurs qui travaillent avec des contrôles Image doivent prendre en charge une propriété pour pouvoir définir la description visuelle sur le contrôle. Cette propriété doit être mappée à la propriété UI Automation **VisualDescription** . |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Consultez les remarques. | Le contrôle image doit être inclus dans l’affichage de contenu de l’arborescence UI Automation lorsqu’il contient des informations significatives qui ne sont pas encore exposées à l’utilisateur final.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle image est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consultez les remarques. | Si le contrôle Image représente des informations d’état sur un élément particulier à l’écran, le contrôle doit être contenu dans l’élément. Lorsque l’image est contenue dans un élément, l’élément doit prendre en charge la propriété Status et déclencher les notifications appropriées lorsque l’état change. Si une image correspond à un contrôle autonome et transmet un état, la propriété Status doit être prise en charge.                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **image** . La valeur par défaut est « image » pour « fr-fr » ou « anglais » (États-Unis).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | La propriété **Name** doit être exposée pour tous les contrôles d’image qui contiennent des informations. Pour accéder par programme à ces informations, il convient de fournir un équivalent textuel du graphique. Si le contrôle d’image est purement décoratif, il doit s’afficher uniquement dans la vue de contrôle de l’arborescence UI Automation et n’a pas besoin d’un nom (consultez la section [Notes](#remarks)). Les infrastructures d’interface utilisateur doivent prendre en charge une propriété de texte de remplacement ou ALT sur les images qu’il est possible de définir dans leur infrastructure. Cette propriété est ensuite mappée à la propriété nom UI Automation.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour les contrôles image. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

| Modèle de contrôle                                                 | Support | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Dépend | Le contrôle image prend en charge le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) si le contrôle se trouve dans un conteneur de grille.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Jamais   | Si le contrôle image est un objet cliquable, le contrôle doit prendre en charge un type de contrôle qui prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , tel que le type de contrôle [Button](uiauto-supportbuttoncontroltype.md) . Pour un objet image qui contient plusieurs objets interversés, l’élément (type de contrôle image) peut héberger des liens enfants (type de contrôle[Hyperlink](uiauto-supporthyperlinkcontroltype.md) ) dans l’arborescence UI Automation. |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Jamais   | Les contrôles image ne doivent pas prendre en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) . Si les images font partie d’un conteneur sélectionnable comme un bouton qui a une icône d’image comme contenu, ce conteneur prend en charge le modèle, et non l’image dans.                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Dépend | Le contrôle image prend en charge le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) si le contrôle se trouve dans un conteneur qui a des contrôles Header.                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’image. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).

| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété ItemStatusPropertyId.               | Si le contrôle prend en charge la propriété [**ItemStatus**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Notes

Le World Wide Web Consortium (W3C) définit une image décorative comme une image qui n’ajoute pas d’informations au contenu d’une page. Pour plus d’informations, consultez la rubrique W3C sur les [images décoratifs](https://www.w3.org/WAI/tutorials/images/decorative/).

En ce qui concerne l’Automation d’interface utilisateur :

- Si une image est purement décorative, n’est pas interactive et ne transmet pas d’informations, l’image :
  - Peut être ou non dans l’arborescence UIA
  - Peut être ou non dans la vue de UIA brut
  - Ne doit pas être dans l’affichage de contrôle UIA
  - Ne doit pas être dans l’affichage de contenu
  - Peut avoir ou non un nom
- Si une image transmet des informations, mais qu’il existe un texte clairement associé qui fournit les mêmes informations (par exemple, un bouton de lecture qui contient un graphique en triangle pointant vers la gauche avec le texte « Play »), l’image est considérée comme décorative et l’image :
  - Doit être dans la vue brute
  - Doit être dans l’affichage de contrôle
  - Ne doit pas être dans l’affichage de contenu
  - Peut avoir ou non une valeur dans la propriété Name
  - Le texte qui indique également la signification de l’image doit être dans l’affichage de contenu
- Si une image est informatif et qu’elle transmet des détails qui ne sont pas fournis par un texte associé, l’image :
  - Doit être dans la vue brute
  - Doit être dans l’affichage de contrôle
  - Doit être dans l’affichage de contenu
  - Doit avoir une valeur de nom qui décrit l’image et sa signification

## <a name="related-topics"></a>Rubriques connexes

### <a name="conceptual"></a>Conceptuel

- [Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
- [Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
