---
title: Modèle de contrôle RangeValue
description: Fournit des instructions et des conventions pour l’implémentation de IRangeValueProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle RangeValue est utilisé pour prendre en charge les contrôles qui peuvent être définis sur une valeur comprise dans une plage.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- UI Automation, implémentation du modèle de contrôle RangeValue
- UI Automation, modèle de contrôle RangeValue
- UI Automation, IRangeValueProvider
- IRangeValueProvider
- implémentation des modèles de contrôle RangeValue d’UI Automation
- Modèles de contrôle RangeValue
- modèles de contrôle, IRangeValueProvider
- modèles de contrôle, implémenter des RangeValue UI Automation
- modèles de contrôle, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010487"
---
# <a name="rangevalue-control-pattern"></a>Modèle de contrôle RangeValue

Fournit des instructions et des conventions pour l’implémentation de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **RangeValue** est utilisé pour prendre en charge les contrôles qui peuvent être définis sur une valeur comprise dans une plage.

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IRangeValueProvider**](#required-members-for-irangevalueprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **RangeValue** , notez les conventions et recommandations suivantes :

-   Les contrôles autorisent le réétalonnage de leurs propriétés prises en charge en fonction des paramètres régionaux ou des préférences de l’utilisateur. Par exemple, vous pouvez définir un contrôle de thermomètre pour afficher la température en degrés Fahrenheit ou Celsius.
-   Les contrôles qui ont des valeurs de plage ambiguës, telles que les barres de progression ou les curseurs, doivent normaliser ces valeurs.

## <a name="required-members-for-irangevalueprovider"></a>Membres requis pour **IRangeValueProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .



| Membres nécessaires                                              | Type de membre | Notes |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | Propriété    | None  |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Propriété    | None  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | Propriété    | None  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Propriété    | None  |
| [**Maximale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Propriété    | None  |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Propriété    | None  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | Méthode      | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




