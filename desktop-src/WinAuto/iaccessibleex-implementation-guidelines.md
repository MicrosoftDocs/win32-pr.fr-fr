---
title: Instructions d’implémentation de IAccessibleEx
description: Le noyau d’automatisation de l’interface utilisateur de Microsoft peut récupérer toutes les propriétés de Active Accessibility Microsoft pour tout objet accessible exposé par un serveur par le biais de l’interface IAccessible.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f2671f3a39a16c99a0d28eeb8a3579f1684b04372c53e1199601bd02f2bcb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929549"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Instructions d’implémentation de IAccessibleEx

Le noyau d’automatisation de l’interface utilisateur de Microsoft peut récupérer toutes les propriétés de Active Accessibility Microsoft pour tout objet accessible exposé par un serveur par le biais de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Lors de l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), vous devez exposer uniquement les aspects des fonctionnalités de l’interface utilisateur qui ne peuvent pas être exposés par ailleurs par le biais des propriétés de Active Accessibility Microsoft existantes. Cette rubrique identifie les propriétés UI Automation et les modèles de contrôle qui représentent les fonctionnalités de l’interface utilisateur qui n’ont pas d’équivalent dans Microsoft Active Accessibility : il s’agit des propriétés et des modèles de contrôle que vous pouvez exposer dans une implémentation de **IAccessibleEx** .

Cette rubrique contient les sections suivantes :

-   [Propriétés](#properties)
-   [Modèles de contrôle](#control-patterns)
-   [WinEvents pour les événements de modification de propriété UI Automation](#winevents-for-ui-automation-property-changed-events)
-   [Rubriques connexes](#related-topics)

## <a name="properties"></a>Propriétés

Les propriétés UI Automation suivantes ne se chevauchent pas avec les fonctionnalités de Microsoft Active Accessibility. Elles peuvent être utilisées dans une implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   AriaProperties
-   AriaRole
-   AutomationId
-   ClassName
-   ClickablePoint
-   ControllerFor
-   Culture
-   DescribedBy
-   FlowsTo
-   FrameworkId
-   IsContentElement
-   IsControlElement
-   IsDataValidForForm
-   IsRequiredForForm
-   ItemStatus
-   itemType
-   LabeledBy
-   LocalizedControlType
-   Orientation

Bien que les propriétés AcceleratorKey et AccessKey UI Automation se chevauchent avec la propriété accKeyboardShortcut Microsoft Active Accessibility, vous pouvez toujours les utiliser dans une implémentation [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour les contrôles qui ont à la fois une touche d’accès rapide et un accélérateur. De même, la propriété ControlType UI Automation chevauche la propriété Microsoft Active Accessibility accRole, mais vous pouvez toujours l’utiliser dans une implémentation **IAccessibleEx** pour définir un rôle plus spécifique pour un contrôle.

Étant donné que les propriétés d’éléments UI Automation suivantes sont déjà couvertes par les propriétés de Microsoft Active Accessibility, il n’est pas nécessaire de les utiliser dans une implémentation [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .



| Propriété UI Automation | Équivalent Microsoft Active Accessibility                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BoundingRectangle      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState, [ **système d’état \_ \_ concentré**](object-state-constants.md)                                                                                       |
| IsEnabled              | accState, [ **système d’état \_ \_ non disponible**](object-state-constants.md)                                                                               |
| IsKeyboardFocusable    | accState, système d’État pouvant être [ **\_ \_ actif**](object-state-constants.md)                                                                                   |
| IsPassword             | accState, [ **système d’état \_ \_ protégé**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Name                   | accName                                                                                                                                                                       |
| NativeWindowHandle     | [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState, [**état \_ système état \_ invisible**](object-state-constants.md) / [**\_ système \_ hors écran**](object-state-constants.md) |
| ProcessId              | Fourni par UI Automation Core                                                                                                                                                |



 

Pour toute propriété UI Automation non prise en charge, votre implémentation de la méthode [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) doit définir le paramètre *pRetVal* sur VT \_ vide et retourner S \_ OK. Le retour de [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) peut entraîner la suppression du mappage par défaut de la propriété correspondante par le proxy MSAA-to-UIA.

## <a name="control-patterns"></a>Modèles de contrôle

Les modèles de contrôle UI Automation suivants ne se chevauchent pas avec les fonctionnalités de Microsoft Active Accessibility. Elles peuvent être utilisées dans une implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   Ancrer
-   ExpandCollapse
-   Grille
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   Table
-   TableItem
-   Transformer

Pour les modèles de contrôle RangeValue et Transform, certaines méthodes se chevauchent entre le modèle de contrôle UI Automation et les méthodes de Active Accessibility de Microsoft. Dans ces cas, les deux doivent être implémentés. Par exemple, les méthodes [**IAccessible :: obtenir \_ AccValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) et [**IAccessible ::P ut \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) de Microsoft Active Accessibility doivent être implémentées, comme les méthodes UI Automation [**IRangeValueProvider :: value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) et [**IRangeValueProvider :: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) . En interne, une implémentation peut partager du code pour ces. Cette condition requise pour implémenter les deux jeux évite d’avoir une implémentation partielle d’une interface de modèle tout en conservant l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilisable par les clients Microsoft Active Accessibility existants.

Les modèles de contrôle UI Automation suivants ne sont pas requis lorsque le contrôle a l’un des rôles décrits ci-dessous ; dans le cas contraire, ils doivent être pris en charge de manière explicite, le cas échéant.



| Modèle de contrôle UI Automation | Rôle de Active Accessibility Microsoft                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Rôle \_ \_Bouton**](object-roles.md)de fonction système, [**système de rôle \_ \_ MenuItem**](object-roles.md), [**\_ \_ BUTTONDROPDOWN**](object-roles.md)de système de rôle, système de rôle [**\_ \_ SPLITBUTTON**](object-roles.md)et tout autre rôle dont la valeur de la propriété accDefaultAction n’est pas **null**. |
| SelectionItemPattern          | [**Rôle \_ \_ListItem système**](object-roles.md), [ **\_ \_ RadioButton du système de rôle**](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**\_liste des systèmes de rôles \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**système de rôle \_ \_ CHECKBUTTON**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Rôle \_ \_Texte système**](object-roles.md) (lorsqu’il n’est pas en lecture seule) [**, \_ \_ PROGRESSBAR, système**](object-roles.md)de rôle, [**\_ \_ ComboBox système**](object-roles.md)et tout autre rôle lorsque la valeur de la propriété accValue n’est pas **null**.                                                                            |
| WindowPattern                 | Pris en charge automatiquement sur les **HWND** Microsoft Win32 de niveau supérieur.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>WinEvents pour les événements de modification de propriété UI Automation

En plus des événements définis pour [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), les identificateurs d’événements suivants sont également définis et peuvent être utilisés avec une implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) comme événements de modification de propriété pour les propriétés UI Automation correspondantes. Celles-ci utilisent le même mécanisme que les événements définis pour **IAccessible**. Pour plus d’informations, consultez [winEvents](winevents-infrastructure.md).



| ID WinEvent pour les implémentations de IAccessibleEx                                                                                              | ID WinEvent connexe de Microsoft Active Accessibility                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ AriaPropertiesPropertyId**](uiauto-automation-element-propids.md)                                    | Aucun                                                                                   |
| [**UIA \_ AriaRolePropertyId**](uiauto-automation-element-propids.md)                                                | Aucun                                                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)                                      | Aucun                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                                          | Aucun                                                                                   |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) | [**EVENT, \_ objet \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ FlowsToPropertyId**](uiauto-automation-element-propids.md)                                                  | Aucun                                                                                   |
| [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md)                                                           | Aucun                                                                                   |
| [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md)                                       | Aucun                                                                                   |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md)                                                   | Aucun                                                                                   |
| [**UIA \_ IsDataValidForFormPropertyId**](uiauto-automation-element-propids.md)                            | Aucun                                                                                   |
| [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)                                              | [**EVENT, \_ objet \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                                            | Aucun                                                                                   |
| [**UIA \_ MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md)                     | Aucun                                                                                   |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md)           | Aucun                                                                                   |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)         | [**CONTENTSCROLLED de l’objet d’événement \_ \_**](event-constants.md) |
| [**UIA \_ ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md)                   | Aucun                                                                                   |
| [**UIA \_ ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md)               | Aucun                                                                                   |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)             | [**CONTENTSCROLLED de l’objet d’événement \_ \_**](event-constants.md) |
| [**UIA \_ ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md)                       | Aucun                                                                                   |
| [**UIA \_ ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md)                                 | [**EVENT, \_ objet \_ STATECHANGE**](event-constants.md)         |



 

Pour les événements ci-dessus qui ont une valeur d’objet d’événement \_ \_ figurant après eux, et l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) doit déclencher cet événement en plus de l’événement de modification indiqué. Cela permet au code client **IAccessibleEx** existant de continuer à fonctionner, tout en transqui transmet des informations d’événement plus granulaires aux clients intéressés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




