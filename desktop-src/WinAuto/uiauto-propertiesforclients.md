---
title: Récupération de propriétés à partir d’éléments UI Automation
description: Les propriétés des objets IUIAutomationElement contiennent des informations sur les éléments d’interface utilisateur, généralement les contrôles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clients, obtention d’éléments UI Automation
- clients, éléments UI Automation
- clients, propriétés
- clients, récupération des propriétés
- clients, propriétés UI Automation
- UI Automation, obtenir des éléments
- UI Automation, éléments
- UI Automation, propriétés
- UI Automation, récupérer des propriétés
- récupération des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292502"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Récupération de propriétés à partir d’éléments UI Automation

Les propriétés des objets [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contiennent des informations sur les éléments d’interface utilisateur, généralement les contrôles. Les propriétés d’un élément sont génériques ; autrement dit, non spécifique à un type de contrôle. Les propriétés spécifiques au contrôle d’un élément sont exposées par ses interfaces de modèle de contrôle.

Les propriétés UI Automation de Microsoft sont en lecture seule. Pour définir les propriétés d’un contrôle, vous devez utiliser les méthodes du modèle de contrôle approprié. Par exemple, utilisez [**IUIAutomationScrollPattern :: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) pour modifier les valeurs de position d’une fenêtre de défilement.

Pour améliorer les performances, les valeurs de propriété des contrôles et des modèles de contrôle peuvent être mises en cache lorsque les éléments sont récupérés. Pour plus d’informations, consultez [Caching UI Automation Properties and Control patterns](uiauto-cachingforclients.md).

Cette rubrique contient les sections suivantes.

-   [ID de propriété](#property-ids)
-   [Conditions de propriété](#property-conditions)
-   [Récupération de propriétés](#retrieving-properties)
-   [Valeurs de propriété par défaut](#default-property-values)
-   [Rubriques connexes](#related-topics)

## <a name="property-ids"></a>ID de propriété

Les identificateurs de propriété sont définis dans UIAutomationClient. h. Ils permettent de spécifier des propriétés lorsque vous vous abonnez à des événements de modification de propriété, de récupérer des valeurs de propriété et de construire des conditions de propriété. Les identificateurs de propriété identifient également la propriété qui a changé lors de l’appel de [**IUIAutomationPropertyChangedEventHandler :: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .

Pour obtenir la liste des identificateurs de propriété UI Automation, consultez [identificateurs de propriété](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Conditions de propriété

Les ID de propriété sont utilisés dans la construction d’objets [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) qui sont utilisés pour rechercher des éléments UI Automation. Par exemple, vous souhaiterez peut-être Rechercher un élément qui a un nom spécifique, ou tous les contrôles qui sont activés. Chaque condition de propriété spécifie un identificateur de propriété et la valeur à laquelle la propriété doit correspondre.

Pour plus d’informations, consultez les rubriques de référence suivantes :

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement :: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement :: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Récupération de propriétés

Certaines propriétés génériques, ainsi que toutes les propriétés de modèle de contrôle, sont disponibles en tant que propriétés sur l’interface du modèle de contrôle ou [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) et peuvent être récupérées à l’aide d’un accesseur, tel que [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).

En outre, toute propriété en cours ou mise en cache (autre que les propriétés de modèle de contrôle) peut être récupérée à l’aide de l’une des méthodes suivantes :

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Ces méthodes offrent des performances légèrement meilleures et un accès à la gamme complète des propriétés. Toutefois, les valeurs sont retournées dans les structures de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , tandis que les accesseurs de propriété individuels effectuent un cast de la valeur vers le type approprié.

## <a name="default-property-values"></a>Valeurs de propriété par défaut

Si un fournisseur UI Automation n’implémente pas de propriété, UI Automation peut fournir une valeur par défaut. Par exemple, si le fournisseur d’un contrôle ne prend pas en charge la propriété identifiée par [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation retourne une chaîne vide. De même, si le fournisseur ne prend pas en charge la propriété identifiée par [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation retourne **false**.

La différence entre [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) et [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (et entre des paires similaires de méthodes) est que la méthode « ex » peut spécifier qu’aucune valeur par défaut ne doit être retournée. Dans ce cas, la valeur de retour est une constante unique spéciale, indiquant que la propriété n’est pas prise en charge. À la réception de cette valeur, l’application peut fournir sa propre valeur ou simplement ignorer la propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Identificateurs de propriété](uiauto-entry-propids.md)
</dt> </dl>

 

 