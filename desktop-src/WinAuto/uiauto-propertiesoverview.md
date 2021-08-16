---
title: Vue d'ensemble des propriétés UI Automation
description: Les fournisseurs UI Automation Microsoft exposent des propriétés sur les éléments UI Automation. Les propriétés permettent aux applications clientes de récupérer des informations sur les contrôles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- UI Automation, vue d’ensemble des propriétés
- UI Automation, propriétés et événements
- UI Automation, événements et propriétés
- Propriétés, à propos de
- Propriétés, identificateurs
- Propriétés, valeurs
- Propriétés, événements
- événements, propriétés
- Propriétés, dynamiques
- propriétés dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745029"
---
# <a name="ui-automation-properties-overview"></a>Vue d'ensemble des propriétés UI Automation

Les fournisseurs UI Automation Microsoft exposent des propriétés sur les éléments UI Automation. Les propriétés permettent aux applications clientes de récupérer des informations sur les contrôles.

UI Automation expose deux types différents de propriétés : les *Propriétés des éléments Automation* et les *propertes de modèle de contrôle*. Les propriétés de l’élément Automation consistent en un ensemble commun de propriétés, telles que Name, AcceleratorKey et ClassName, qui sont exposées par tous les éléments UI Automation, quel que soit le type de contrôle. La plupart des propriétés d’élément Automation sont des valeurs statiques.

Les propriétés de modèle de contrôle sont celles qui sont exposées par un contrôle qui prend en charge un modèle de contrôle particulier. Chaque modèle de contrôle a un ensemble correspondant de propriétés de modèle de contrôle que le contrôle doit exposer. Par exemple, un contrôle qui prend en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) expose les propriétés ColumnCount et RowCount. La plupart des propriétés de modèle de contrôle sont des valeurs dynamiques.

Cette rubrique contient les sections suivantes.

-   [Identificateurs de propriété](#property-identifiers)
-   [Valeurs de propriété](#property-values)
-   [Propriétés et événements](#properties-and-events)
-   [Rubriques connexes](#related-topics)

## <a name="property-identifiers"></a>Identificateurs de propriété

Chaque propriété est identifiée par une valeur de type **PROPERTYID** appelée *identificateur de propriété* (ID). Les fournisseurs et les clients utilisent les ID numériques dans les appels de méthode tels que [**IRawElementProviderAdviseEvents :: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) et [**IUIAutomationElement :: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) pour identifier les demandes de propriété. Pour obtenir une description détaillée de chaque identificateur de propriété UI Automation, y compris le type de données et la valeur par défaut de chaque propriété, consultez [identificateurs de propriété](uiauto-entry-propids.md).

## <a name="property-values"></a>Valeurs de la propriété

Toutes les propriétés sont en lecture seule, même si certaines peuvent être modifiées à l’aide de méthodes qui agissent sur le contrôle, telles que [**IDockProvider :: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) ou [**IUIAutomationDockPattern :: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).

Pour plus d’informations sur la récupération des valeurs de propriété, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Propriétés et événements

Le concept des *événements de modification de propriété* est étroitement associé aux propriétés d’UI Automation. Pour les propriétés dynamiques, une application cliente a besoin d’un moyen de savoir qu’une valeur de propriété a changé, afin qu’elle puisse mettre à jour son cache d’informations ou réagir aux nouvelles informations d’une autre façon. Les clients peuvent s’inscrire pour écouter les événements de modification de propriété sur n’importe quelle propriété.

Les fournisseurs déclenchent des événements quand un événement de l’interface utilisateur change. Par exemple, si une case à cocher est activée ou désactivée, un événement de modification de propriété est déclenché par l’implémentation du fournisseur du modèle de contrôle [Toggle](uiauto-implementingtoggle.md) . Les fournisseurs peuvent déclencher des événements de manière sélective, selon que les clients écoutent tous les événements ou seulement des événements spécifiques.

Toutes les modifications de propriété ne déclenchent pas nécessairement des événements. Cela dépend entièrement de l’implémentation du fournisseur UI Automation pour l’élément. Par exemple, les fournisseurs de proxy standard pour les zones de liste ne déclenchent pas d’événement de modification de propriété lorsque la propriété de sélection change. Dans ce cas, l’application doit écouter l’événement déclenché lorsque la sélection change ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Les clients écoutent les événements en s’abonnant à eux, comme décrit dans [abonnement à des événements UI Automation](uiauto-eventsforclients.md). Pour les événements de modification de propriété en particulier, les clients doivent implémenter [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) et passer l’interface à [**IUIAutomation :: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**IUIAutomation :: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 




