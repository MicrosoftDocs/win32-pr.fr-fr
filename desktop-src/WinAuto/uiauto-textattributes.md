---
title: Attributs de texte UI Automation
description: Cette rubrique décrit comment Microsoft UI Automation expose les propriétés de mise en forme et de style (attributs de texte) du contenu textuel et fournit une liste d’attributs de texte pris en charge.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- UI Automation, attributs de texte
- attributs de texte, à propos de
- attributs de texte, types variant
- attributs de texte, types de données
- UI Automation, liste d’attributs
- UI Automation, liste des attributs de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520545"
---
# <a name="ui-automation-text-attributes"></a>Attributs de texte UI Automation

Cette rubrique décrit comment Microsoft UI Automation expose les propriétés de mise en forme et de style (*attributs de texte*) du contenu textuel et fournit une liste d’attributs de texte pris en charge.

Les fournisseurs UI Automation exposent des attributs de texte par le biais des méthodes [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) et [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) du modèle de contrôle [TextRange](uiauto-about-text-and-textrange-patterns.md) . Les applications clientes utilisent la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) pour récupérer la valeur d’un attribut de texte particulier pour une plage de texte. Les clients peuvent utiliser la méthode [**IUIAutomationTextRange :: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) pour rechercher dans une plage de texte un texte ayant un attribut particulier. Si un texte correspondant est trouvé, la méthode crée une nouvelle plage de texte qui contient le texte correspondant.

Les attributs de texte de la liste suivante sont pris en charge par le modèle de contrôle **TextRange** . Les noms d’attributs sont dérivés des identificateurs d’attribut de texte UI Automation. Par exemple, l’attribut **AnimationStyle** est identifié par les clients en tant que [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (défini dans UIAutomationClient. h) et par les fournisseurs comme **texte \_ \_ \_ GUID d’attribut AnimationStyle** (défini dans Uiautomationcoreapi. h). Pour plus d’informations sur chaque attribut de texte pris en charge, consultez [**identificateurs d’attribut de texte**](uiauto-textattribute-ids.md).

> [!Note]  
> Certains des attributs répertoriés sont pris en charge à partir de Windows 8. Consultez [**identificateurs d’attribut de texte**](uiauto-textattribute-ids.md) pour les notes relatives à la prise en charge des versions.

 

Cette rubrique contient les sections suivantes :

-   [Attributs d'annotation](#annotation-attributes)
-   [Attributs de police](#font-attributes)
-   [Attributs de langage](#language-attributes)
-   [Attribut de lien](#link-attribute)
-   [Attributs de marge de page](#page-margin-attributes)
-   [Attributs d’alignement de texte](#text-alignment-attributes)
-   [Attributs de couleur de texte](#text-color-attributes)
-   [Attributs de décoration de texte](#text-decoration-attributes)
-   [Attributs de style de texte](#text-style-attributes)
-   [Attributs d’interaction et de sélection](#interaction-and-selection-attributes)
-   [Rubriques connexes](#related-topics)

## <a name="annotation-attributes"></a>Attributs d'annotation

Les objets d’annotation et les types d’annotation sont disponibles par le biais des attributs suivants.



| Attribut             | Identificateur                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-annotation-type-identifiers.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a>Attributs de police

Le nom, la taille et le poids d’une police sont disponibles par le biais des attributs suivants.



| Attribut      | Identificateur                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Attributs de langage

Les informations relatives à la langue du texte sont disponibles par le biais des attributs suivants.



| Attribut              | Identificateur                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Culturel**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Attribut de lien

L’attribut suivant fournit la plage de texte qui est la cible d’un lien dans un document.



| Attribut | Identificateur                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Lien**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Attributs de marge de page

Les rectangles englobants d’une plage de texte n’exposent pas les coordonnées du texte dans la page. Toutefois, un fournisseur peut exposer les informations sur les marges de page à l’aide des attributs de texte suivants.



| Attribut          | Identificateur                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Attributs d’alignement de texte

Les informations relatives à l’alignement du texte, telles que la mise en retrait, les paramètres d’onglet et l’alignement horizontal, sont disponibles par le biais des attributs suivants.



| Attribut                   | Identificateur                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Tabulations**                    | [**UIA \_ TabsAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Attributs de couleur de texte

Les couleurs de texte de premier plan et d’arrière-plan sont disponibles via les attributs de texte suivants. Les deux couleurs sont spécifiées en tant que type de données [**COLORREF**](/windows/desktop/gdi/colorref) .



| Attribut           | Identificateur                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Attributs de décoration de texte

Les décorations de texte incluent des zones telles que les puces, le soulignement et les animations. Si le texte inclut des puces ou des nombres de début, le symbole ou le texte utilisé pour la puce ou le numéro doit être inclus dans le flux de texte, le cas échéant.

Des informations sur les décorations de texte sont disponibles par le biais des attributs suivants.



| Attribut              | Identificateur                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **BulletStyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Attributs de style de texte

Des informations sur les styles de texte sont disponibles via les attributs suivants.



| Attribut         | Identificateur                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Attributs d’interaction et de sélection

Les informations relatives à la sélection de texte en cours dans la plage et l’état du focus sont disponibles via les attributs suivants.



| Attribut              | Identificateur                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[À propos du texte UI Automation et des modèles de contrôle TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Modèles de contrôle Text et TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 