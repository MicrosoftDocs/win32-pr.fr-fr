---
title: Styles (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IStylesProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle styles est utilisé pour décrire un élément d’interface utilisateur doté d’un style, d’une couleur de remplissage, d’un motif de remplissage ou d’une forme spécifique.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- UI Automation, implémenter le modèle de contrôle des styles
- UI Automation, modèle de contrôle des styles
- UI Automation, IStylesProvider
- IStylesProvider
- implémentation du modèle de contrôle des styles UI Automation
- Styles (modèle de contrôle)
- modèles de contrôle, IStylesProvider
- modèles de contrôle, implémenter des styles UI Automation
- modèles de contrôle, styles
- interfaces, IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729604"
---
# <a name="styles-control-pattern"></a>Styles (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **styles** est utilisé pour décrire un élément d’interface utilisateur doté d’un style, d’une couleur de remplissage, d’un motif de remplissage ou d’une forme spécifique.

Le modèle de contrôle **styles** est particulièrement utile pour décrire des éléments dans un document, qui ont souvent ces styles. Les styles contiennent généralement des informations qui sont utiles pour les clients handicapés ; par exemple, un style peut décrire une certaine chaîne comme titre d’un document ou un certain objet Flowchart comme un losange ou un cercle. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IStylesProvider**](#required-members-for-istylesprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **styles** , notez les conventions et recommandations suivantes :

-   Le fichier d’en-tête UIAutomationClient. h définit un ensemble de valeurs constantes nommées utilisées pour identifier plusieurs styles courants. Pour plus d’informations, consultez [**identificateurs de style**](uiauto-style-identifiers.md).
-   Si vous utilisez [**StyleId \_ Custom**](uiauto-style-identifiers.md), vous devez implémenter la propriété [**IStylesProvider :: styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) pour permettre aux clients de découvrir le nom du style. Vous n’avez pas besoin d’implémenter la propriété **styleName** pour un style standard, car Microsoft UI Automation fournit un nom par défaut, mais vous pouvez l’implémenter si vous devez remplacer le nom par défaut.
-   Les autres propriétés dans le modèle de **styles** sont facultatives. le fournisseur peut retourner [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) pour une propriété qui n’est pas prise en charge.
-   Les styles d’une plage de texte peuvent être représentés à l’aide des attributs de texte suivants :
    -   Lors de la réponse à une demande pour l’attribut de texte [**StyleId**](uiauto-textattribute-ids.md) , la plage de texte doit retourner l’un des identificateurs de style décrits dans [**identificateurs de style**](uiauto-style-identifiers.md).
    -   Si [**StyleId \_ personnalisé**](uiauto-style-identifiers.md) est utilisé, la plage de texte doit retourner une valeur de chaîne pour l’attribut de texte [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) pour permettre aux clients de découvrir le nom du style.
    -   Une plage de texte qui a plusieurs styles, tels que le titre et le texte normal, doit retourner la propriété [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) spéciale UI Automation pour les propriétés [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) et [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) . Un client recevant cette réponse peut subdiviser la plage de texte pour Rechercher l’endroit où les styles commencent et se terminent.
-   Les applications peuvent utiliser un large éventail de styles pour décrire les objets, mais UI Automation représente uniquement les plus courants. Pour représenter des attributs de style supplémentaires, tels que la couleur de bordure, un fournisseur peut retourner une liste d’attributs supplémentaires dans la propriété [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) . Il s’agit fondamentalement d’un conteneur de propriétés avec un ensemble de propriétés étendues, telles que «BorderColor = 0xFF0000 ; BorderStyle = pointillés». Les valeurs des propriétés étendues peuvent être spécifiques à l’application.

## <a name="required-members-for-istylesprovider"></a>Membres requis pour **IStylesProvider**

Les propriétés suivantes sont requises pour implémenter l’interface [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) .



| Membres nécessaires                                                            | Type de membre | Notes |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Propriété    | Aucun  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Propriété    | Aucun  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Propriété    | Aucun  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Propriété    | Aucun  |
| [**Graphique à base de formes**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Propriété    | Aucun  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Propriété    | Aucun  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Propriété    | Aucun  |



 

Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 