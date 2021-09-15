---
title: Annotation (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IAnnotationProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle d’annotation est utilisé pour exposer les propriétés d’une annotation dans un document.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- UI Automation, implémenter le modèle de contrôle d’annotation
- UI Automation, modèle de contrôle d’annotation
- UI Automation, IAnnotationProvider
- IAnnotationProvider
- implémentation du modèle de contrôle d’annotation UI Automation
- annotation (modèle de contrôle)
- modèles de contrôle, IAnnotationProvider
- modèles de contrôle, implémenter une annotation UI Automation
- modèles de contrôle, annotation
- interfaces, IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a0441816e548faaa9076b3a9717c0aa76f08a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518101"
---
# <a name="annotation-control-pattern"></a>Annotation (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle d' **annotation** est utilisé pour exposer les propriétés d’une annotation dans un document.

Par exemple, une bulle de commentaire se trouve dans la marge d’un document et est connectée à un texte de document ou à une cellule de feuille de calcul.

L’illustration suivante montre un exemple d’annotation. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

![capture d’écran montrant un commentaire baloon dans un document](images/annotation.png)

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle d' **annotation** , notez les conventions et recommandations suivantes :

-   Il existe de nombreux types d’annotations. Le fichier d’en-tête UIAutomationClient. h définit un ensemble de valeurs constantes nommées qui identifient les types d’annotations pris en charge par Microsoft UI Automation. Pour plus d’informations, consultez [**identificateurs de type d’annotation**](uiauto-annotation-type-identifiers.md).
-   Si vous utilisez [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md), vous devez implémenter la propriété [**IAnnotationProvider :: AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) pour permettre aux clients de découvrir le nom du type d’annotation. Vous n’avez pas besoin d’implémenter **AnnotationTypeName** pour un type d’annotation standard, car UI Automation fournit un nom par défaut, mais vous pouvez l’implémenter si vous devez remplacer le nom par défaut.
-   La propriété [**IAnnotationProvider :: Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) est facultative.
-   La propriété [**IAnnotationProvider ::D atetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) est facultative.
-   La propriété [**IAnnotationProvider :: target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) est obligatoire, car elle lie une annotation à un élément d’interface utilisateur, ce qui permet à un client de naviguer de l’annotation vers l’élément d’interface utilisateur auquel l’annotation fait référence.
-   Étant donné que les annotations peuvent prendre de nombreuses formes, l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) ne définit pas de propriété pour stocker la valeur ou le texte d’une annotation. Une annotation simple doit exposer l’interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) , et la propriété [**IValueProvider :: value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) doit retourner une valeur en lecture seule qui spécifie le texte de l’annotation. Une annotation plus riche doit exposer l’interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) pour fournir du texte plus riche aux clients.
-   La navigation à partir d’un élément d’interface utilisateur vers une annotation sur l’élément dépend du type d’élément qui est annoté, comme suit :
    -   Pour les cellules de feuille de calcul, implémentez la méthode [**ISpreadsheetItemProvider :: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) pour faire référence à l’annotation.
    -   Pour le contenu textuel, implémentez l’attribut de texte [**AnnotationObjects**](uiauto-textattribute-ids.md) sur l’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) pour faire référence à l’annotation.
-   Certains types d’annotations ne nécessitent pas une implémentation complète de l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Par exemple, un indicateur d’erreur orthographique simple peut être représenté en faisant en sorte que l’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) retourne un attribut [**AnnotationTypes**](uiauto-textattribute-ids.md) Text de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)et une valeur null pour l’attribut Text [**AnnotationObjects**](uiauto-textattribute-ids.md) .
-   Il peut être utile d’implémenter l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) sur un élément d’interface utilisateur qui n’est pas visible. Par exemple, vous pouvez créer un élément UI Automation non visible qui implémente **IAnnotationProvider** pour fournir des informations étendues sur une erreur de grammaire.
-   Les annotations dans un contrôle textuel peuvent être complexes si le contrôle contient des commentaires qui se chevauchent. Utilisez les instructions suivantes pour gérer les annotations complexes :
    -   Une plage de texte sans annotations doit retourner un tableau vide pour l’attribut de texte [**AnnotationTypes**](uiauto-textattribute-ids.md) et un tableau vide pour l’attribut de texte [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Une plage de texte avec une annotation doit retourner un tableau d’une valeur entière pour l’attribut [**AnnotationTypes**](uiauto-textattribute-ids.md) Text et un tableau d’une interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour l’attribut Text [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Une plage de texte avec plusieurs annotations doit retourner un tableau de plusieurs valeurs entières pour l’attribut [**AnnotationTypes**](uiauto-textattribute-ids.md) Text et un tableau d’un nombre correspondant d’interfaces [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour l’attribut Text [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Une plage de texte avec des annotations variables, telle qu’une plage avec du texte annoté et non annoté, doit retourner la propriété [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) pour [**AnnotationTypes**](uiauto-textattribute-ids.md) et [**AnnotationObjects**](uiauto-textattribute-ids.md). Un client recevant cette réponse peut subdiviser la plage de texte pour Rechercher l’endroit où les annotations commencent et se terminent.

## <a name="required-members-for-iannotationprovider"></a>Membres requis pour **IAnnotationProvider**

Les propriétés suivantes sont requises pour implémenter l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .



| Membres nécessaires                                                                | Type de membre | Notes |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Propriété    | Aucun. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Propriété    | Aucun. |
| [**Auteur**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Propriété    | Aucun. |
| [**DateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Propriété    | Aucun. |
| [**Cible**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Propriété    | Aucun. |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 