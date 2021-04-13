---
title: Value (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IValueProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- UI Automation, implémenter le modèle de contrôle value
- UI Automation, modèle de contrôle de valeur
- UI Automation, IValueProvider
- IValueProvider
- implémentation des modèles de contrôle value d’UI Automation
- Modèles de contrôle de valeur
- modèles de contrôle, IValueProvider
- modèles de contrôle, implémenter la valeur UI Automation
- modèles de contrôle, valeur
- interfaces, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382295"
---
# <a name="value-control-pattern"></a>Value (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **value** est utilisé pour prendre en charge les contrôles qui ont une valeur intrinsèque qui ne couvre pas une plage et qui peuvent être représentés sous forme de chaîne.

La chaîne de valeur peut être modifiable, en fonction du contrôle et de ses paramètres. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IValueProvider**](#required-members-for-ivalueprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **value** , notez les conventions et recommandations suivantes :

-   Les contrôles tels qu’un élément de liste ou un élément d’arborescence doivent prendre en charge le modèle de contrôle **value** si la valeur de l’un des éléments est modifiable, quel que soit le mode d’édition actuel du contrôle. Le contrôle parent doit également prendre en charge le modèle de contrôle **value** si les éléments enfants sont modifiables. L’illustration suivante montre un exemple d’élément de liste modifiable.

    ![Illustration montrant un élément de liste modifiable](images/uia-valuepattern-editable-listitem.jpg)

- Les contrôles d’édition à une seule ligne et à plusieurs lignes doivent implémenter [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) pour exposer leur contenu en lecture seule.
- Les contrôles d’édition sur plusieurs lignes doivent implémenter [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) si leur contenu peut être modifié.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) ne prend pas en charge la récupération des informations de mise en forme ou des valeurs de sous-chaîne. Implémentez [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) dans ces scénarios.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) doit être implémenté par des contrôles tels que le contrôle de sélection de sélecteur de couleurs de Microsoft Word (Voir l’image suivante), qui prend en charge le mappage de chaînes entre une valeur de couleur (par exemple, « jaune ») et une valeur [RVB](/windows/win32/api/wingdi/nf-wingdi-rgb) interne équivalente.

    ![Illustration montrant le mappage de la chaîne d’échantillons de couleurs](images/uia-valuepattern-colorpicker.jpg)

- La propriété **IsEnabled** d’un contrôle doit avoir la valeur **true** et sa propriété [**ITextProvider :: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) la valeur **false** avant d’autoriser un appel à [**ITextProvider :: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).

## <a name="required-members-for-ivalueprovider"></a>Membres requis pour **IValueProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .



| Membres nécessaires                                       | Type de membre | Notes |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Propriété    | Aucun  |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Propriété    | Aucun  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Méthode      | Aucun  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Modèles de contrôle Text et TextRange](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 