---
title: Modèle de contrôle TextChild
description: Présente des recommandations et des conventions pour l’implémentation de ITextChildProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle TextChild est utilisé pour accéder à l’ancêtre le plus proche d’un élément qui prend en charge le modèle de contrôle Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- UI Automation, implémentation du modèle de contrôle TextChild
- UI Automation, modèle de contrôle TextChild
- UI Automation, ITextChildProvider
- ITextChildProvider
- implémentation des modèles de contrôle TextChild d’UI Automation
- Modèles de contrôle TextChild
- modèles de contrôle, ITextChildProvider
- modèles de contrôle, implémenter des TextChild UI Automation
- modèles de contrôle, TextChild
- interfaces, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729956"
---
# <a name="textchild-control-pattern"></a>Modèle de contrôle TextChild

Présente des recommandations et des conventions pour l’implémentation de [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **TextChild** est utilisé pour accéder à l’ancêtre le plus proche d’un élément qui prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) .

Supposons, par exemple, que le texte d’un document contient une image incorporée et un lien hypertexte, comme illustré dans l’image suivante.

![capture d’écran montrant du texte contenant une image incorporée et un lien hypertexte](images/textchild-pattern.png)

Si vous utilisez les outils d’automatisation d’interface utilisateur de Microsoft pour examiner l’arborescence UI Automation pour le contenu de ce document, il est possible qu’il affiche un élément de document avec un élément enfant qui représente l’image, et un autre élément enfant qui représente le lien hypertexte. Par exemple :

![capture d’écran montrant un exemple d’arborescence d’éléments UI Automation](images/textchild-pattern-tree.png)

En général, l’élément de document dans l’exemple précédent prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , mais pas les deux enfants de l’élément de document. Si une application cliente UI Automation a une référence à l’élément image ou à l’élément Hyperlink, le client peut utiliser le modèle de contrôle **TextChild** comme un moyen pratique d’accéder au modèle TextControl exposé par l’élément de document conteneur.

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez l’interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , notez les conventions et recommandations suivantes :

-   La propriété [**ITextChildProvider :: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) doit spécifier l’élément ancêtre le plus proche qui prend en charge l’interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , que les éléments situés plus haut dans la chaîne ancêtre prennent également en charge **ITextProvider**.
-   Un élément ne doit pas prendre en charge à la fois [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et l’interface [ITextChildProvider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .
- Un élément qui implémente [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) doit être un enfant ou un descendant d’un élément qui implémente [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider). Il n’est pas nécessaire que cet élément implémente également le [modèle de contrôle Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   La propriété [**ITextChildProvider :: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) doit spécifier la même plage de texte que celle que l’élément de fournisseur de texte conteneur retourne lorsque sa fonction [**ITextProvider :: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) est appelée avec l’élément enfant Text en tant qu’élément enfant délimité.

## <a name="required-members-for-itextchildprovider"></a>Membres requis pour **ITextChildProvider**

Ces propriétés et méthodes sont requises pour implémenter l’interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .



| Membres nécessaires                                                     | Type de membre | Notes |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Propriété    | Aucun  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Propriété    | Aucun  |



 

Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.

## <a name="related-topics"></a>Rubriques connexes

**Méthodologique**

- [Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
- [Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
- [Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)