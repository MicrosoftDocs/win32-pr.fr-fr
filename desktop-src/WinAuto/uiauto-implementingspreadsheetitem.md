---
title: Modèle de contrôle SpreadsheetItem
description: Fournit des instructions et des conventions pour l’implémentation de ISpreadsheetItemProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- UI Automation, implémentation du modèle de contrôle SpreadsheetItem
- UI Automation, modèle de contrôle SpreadsheetItem
- UI Automation, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implémentation du modèle de contrôle SpreadsheetItem d’UI Automation
- Modèle de contrôle SpreadsheetItem
- modèles de contrôle, ISpreadsheetItemProvider
- modèles de contrôle, implémenter des SpreadsheetItem UI Automation
- modèles de contrôle, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031728"
---
# <a name="spreadsheetitem-control-pattern"></a>Modèle de contrôle SpreadsheetItem

Fournit des instructions et des conventions pour l’implémentation de [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **SpreadsheetItem** est utilisé pour exposer les propriétés d’une cellule dans une feuille de calcul ou un autre document basé sur la grille.

Le modèle de contrôle **SpreadsheetItem** est étroitement lié au modèle de contrôle [GridItem](uiauto-implementinggriditem.md) . les contrôles qui implémentent le modèle de contrôle **SpreadsheetItem** doivent également implémenter le modèle de contrôle GridItem. Les contrôles peuvent également implémenter le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) , le cas échéant. Pour obtenir des exemples de contrôles qui implémentent ces modèles de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **SpreadsheetItem** , notez les conventions et recommandations suivantes :

-   Lorsque vous implémentez les méthodes [**ISpreadsheetItemProvider :: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) et [**ISpreadsheetItemProvider :: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , reportez-vous à la documentation [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Ces méthodes retournent des tableaux pour permettre aux fournisseurs de prendre en charge plusieurs annotations sur une seule cellule.
-   Certains types d’annotations ne nécessitent pas une implémentation complète de l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Par exemple, un indicateur d’erreur d’orthographe simple peut être représenté en indiquant que [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) retourne un identificateur d’attribut de texte de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)et que [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) retourne une valeur null.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Membres requis pour **ISpreadsheetItemProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .



| Membres nécessaires                                                                         | Type de membre | Notes                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formule**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Propriété    | L’implémentation d’une propriété de [**formule**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) distincte est nécessaire, car la propriété de [valeur](value-property.md) d’une cellule retourne généralement la valeur calculée de la cellule. La propriété **Formula** doit avoir la **valeur null** si aucune formule n’est définie. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Méthode      | Retourne un tableau de fournisseurs d’éléments qui font référence aux annotations liées à cette cellule. Les pointeurs dans le tableau peuvent avoir la valeur null si une annotation n’a pas de fournisseur lié.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Méthode      | Retourne un tableau d’identificateurs de type d’annotation qui décrivent les annotations sur cette cellule. Le tableau doit avoir la même taille que le tableau retourné par [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Spreadsheet (modèle de contrôle)](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 