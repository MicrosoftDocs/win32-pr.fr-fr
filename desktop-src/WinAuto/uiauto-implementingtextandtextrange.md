---
title: Modèles de contrôle Text et TextRange
description: Fournit des instructions et des conventions pour l’implémentation de ITextProvider, ITextProvider2 et ITextRangeProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- UI Automation, implémenter le modèle de contrôle Text
- UI Automation, implémenter le modèle de contrôle TextRange
- UI Automation, modèle de contrôle de texte
- UI Automation, modèle de contrôle TextRange
- UI Automation, ITextProvider
- UI Automation, ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- implémentation du modèle de contrôle Text d’UI Automation
- implémentation du modèle de contrôle TextRange d’UI Automation
- Text (modèle de contrôle)
- TextRange (modèle de contrôle)
- modèles de contrôle, ITextProvider
- modèles de contrôle, ITextRangeProvider
- modèles de contrôle, implémenter du texte UI Automation
- modèles de contrôle, implémentation d’UI Automation TextRange
- modèles de contrôle, texte
- modèles de contrôle, TextRange
- interfaces, ITextProvider
- interfaces, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403982"
---
# <a name="text-and-textrange-control-patterns"></a>Modèles de contrôle Text et TextRange

Fournit des instructions et des conventions pour l’implémentation de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)et [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Text** permet aux applications et aux contrôles d’exposer un modèle d’objet de texte simple, permettant ainsi aux clients d’extraire du contenu textuel, des attributs de texte et des objets incorporés à partir de contrôles textuels.

Pour prendre en charge le modèle de contrôle **Text** , les contrôles implémentent les interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) . Les types de contrôle qui doivent prendre en charge le modèle de contrôle **Text** incluent les types de contrôle de [modification](uiauto-supporteditcontroltype.md) et de [document](uiauto-supportdocumentcontroltype.md) , ainsi que tout autre type de contrôle qui permet à l’utilisateur d’entrer du texte ou de sélectionner du texte en lecture seule.

Le modèle de contrôle **Text** peut être utilisé avec d’autres modèles de contrôle Microsoft UI Automation pour prendre en charge plusieurs types d’objets incorporés dans le texte, y compris les tables, les liens hypertexte et les boutons de commande.

Les interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) incluent un certain nombre de méthodes pour acquérir des plages de texte. Une *plage de texte* est un objet qui représente une étendue contiguë de texte, ou plusieurs étendues disjointes de texte, dans un conteneur de texte. Une méthode **ITextProvider** acquiert une plage de texte qui représente l’intégralité du document, tandis que d’autres acquièrent des plages de texte qui représentent une partie du document, telles que le texte sélectionné, le texte visible ou un objet incorporé dans le texte.

Un objet de plage de texte est représenté par le modèle de contrôle **TextRange** , qui est implémenté par le biais de l’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Le modèle de contrôle **TextRange** fournit des méthodes et des propriétés utilisées pour exposer des informations sur le texte de la plage, déplacer les points de terminaison de la plage, sélectionner ou désélectionner du texte, faire défiler la plage dans la vue, et ainsi de suite.

Pour plus d’informations sur les modèles de contrôle **Text** et **TextRange** , consultez [prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md).

à partir de Windows 8.1 fournisseurs peuvent implémenter l’interface [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) . Cela permet d’appeler des menus contextuels associés à une plage de texte. Cela prend en charge des scénarios tels que la correction automatique de texte ou la sélection de candidat de l’éditeur de méthode d’entrée (IME).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ITextProvider**](#required-members-for-itextprovider)
-   [Membres requis pour **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Prise en charge des plages de texte](#supporting-text-ranges)
    -   [Manipulation d’une plage de texte par unité de texte](#manipulating-a-text-range-by-text-unit)
    -   [Sélection de texte dans une plage de texte](#selecting-text-in-a-text-range)
    -   [Acquisition de texte à partir d’une plage de texte](#acquiring-text-from-a-text-range)
    -   [Implémentation de ShowContextMenu](#implementing-showcontextmenu)
-   [Interopérabilité avec le signe insertion du système](#interoperability-with-the-system-caret)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Text** , notez les conventions et recommandations suivantes :

-   Tout contrôle qui permet d’accéder à du texte (par exemple, en entrant du texte ou en sélectionnant du texte en lecture seule) doit prendre en charge le modèle de contrôle **Text** .
-   Le modèle de contrôle **Text** peut être utilisé avec n’importe quel élément d’interface utilisateur qui présente du texte, même une étiquette statique sur un contrôle bouton standard. Toutefois, il n’est pas obligatoire sur les contrôles de texte statiques qui ne peuvent pas être sélectionnés ou qui n’ont pas de point d’insertion.
-   Pour vous assurer que le texte est entièrement accessible, les contrôles qui implémentent [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) doivent également prendre en charge l’interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) . **IValueProvider** complète **ITextProvider** en fournissant un moyen par programmation de modifier le texte. Il offre également une meilleure compatibilité avec les applications clientes de technologie d’assistance, y compris celles basées sur des technologies héritées telles que Microsoft Active Accessibility. Lorsque les deux modèles de contrôle sont implémentés, l’événement **TextChanged** ([**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)) et **AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) sont équivalents pour la propriété **value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Les deux événements doivent être pris en charge.
-   Le modèle de contrôle **Text** ne prend en charge qu’un seul flux de texte et une seule fenêtre d’affichage par contrôle. Si l’application propose plusieurs vues de document dans des volets, chaque vue (contrôle) doit prendre en charge [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) indépendamment.
-   La méthode [**ITextProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) peut retourner une seule plage de texte représentant le texte actuellement sélectionné. Si un contrôle prend en charge la sélection de plusieurs étendues non contiguës de texte, la méthode **GetSelection** doit retourner un tableau qui contient une interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) pour chaque étendue de texte sélectionnée.
-   Le modèle de contrôle **Text** représente le point d’insertion sous la forme d’une plage de texte dégénérée (vide). La méthode [**ITextProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) doit retourner une plage de texte dégénérée lorsque le point d’insertion existe et qu’aucun texte n’est sélectionné. Pour plus d’informations, consultez [interopérabilité avec le signe insertion du système](#interoperability-with-the-system-caret).
-   La méthode [**ITextProvider :: GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) peut retourner une seule plage de texte si une plage contiguë de texte est visible dans la fenêtre d’affichage, ou elle peut retourner un tableau de plages de texte disjointes représentant plusieurs lignes de texte partiellement visibles.
-   La méthode [**ITextProvider :: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) doit retourner une plage dégénérée si l’élément enfant ne contient pas de texte. Comme un objet incorporé peut inclure du texte, la méthode **RangeFromChild** ne retourne pas toujours une plage de texte dégénérée. Pour plus d’informations, consultez [Comment UI Automation expose des objets incorporés](uiauto-textpattern-and-embedded-objects-overview.md).
-   La méthode [**ITextProvider :: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) effectue un test de positionnement dans la zone de document à l’aide des coordonnées d’écran spécifiées. La plage de texte résultante doit être cohérente avec le point d’insertion ou la sélection qui résulterait d’un clic sur l’emplacement aux coordonnées d’écran spécifiées. Par exemple, si une image réside aux coordonnées d’écran spécifiées, la plage de texte résultante doit être la même que la plage de texte que la méthode [**ITextProvider :: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) obtient pour l’image. De même, si une application cliente demande une plage de texte pour l’emplacement au centre du signe insertion du système (point d’insertion), la plage de texte résultante doit être identique à l’emplacement du signe insertion du système.
-   La propriété [**ITextProvider ::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) doit toujours fournir une plage de texte qui comprend tout le texte pris en charge par l’implémentation [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) correspondante.
-   L' [**événement \_ \_ TextChangedEventId de texte UIA**](uiauto-event-ids.md) doit être déclenché après toute modification de texte, même si la modification n’est pas visible dans la fenêtre d’affichage. Par exemple, le fournisseur doit déclencher l’événement même si l’utilisateur colle exactement le même texte sur le texte sélectionné.
-   Le [**\_ \_ TextSelectionChangedEventId de texte UIA**](uiauto-event-ids.md) doit être déclenché chaque fois que la sélection de texte change, ou chaque fois que le point d’insertion (signe insertion) se déplace entre le texte.

Lorsque vous implémentez le modèle de contrôle **TextRange** , notez les conventions et recommandations suivantes :

-   Toutes les méthodes du modèle de contrôle **TextRange** doivent effectuer des opérations de texte indépendamment de l’état de visibilité du texte. La visibilité d’une plage de texte peut toujours être déterminée en interrogeant l’attribut de texte **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Si possible, un fournisseur doit s’assurer que les modifications de texte, telles que les suppressions, les insertions et les déplacements, sont reflétées dans les objets de la plage de texte associée (instances de l’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ) et déclencher un événement de [**\_ \_ TextChangedEventId de texte UIA**](uiauto-event-ids.md) . Les clients peuvent utiliser l’événement comme indication pour confirmer les modifications éditoriales apportées au texte d’un contrôle.
-   Tous les objets de la plage de texte utilisés par les méthodes [**ITextRangeProvider :: compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**compareEndPoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)et [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) doivent être des homologues de la même implémentation du modèle de contrôle de **texte** .
-   Bien que cela ne soit pas obligatoire, la valeur *pRetVal* récupérée par la méthode [**ITextRangeProvider :: CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) peut indiquer la distance, en caractères ([**\_ caractère TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), entre les deux points de terminaison. Toutefois, les applications clientes ne doivent pas dépendre de la précision de *pRetVal* au-delà de sa valeur positive ou négative.
-   Les méthodes [**ITextRangeProvider :: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit), [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)et [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) requièrent une attention particulière pour l’unité de texte spécifiée. Pour plus d’informations, consultez manipulation d’un TextRange par unité de texte.
-   Pour connaître les conditions d’implémentation liées aux méthodes [**ITextRangeProvider :: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)et [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) , consultez sélection de texte dans une plage de texte.
-   Les méthodes [**ITextRangeProvider :: FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) et [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) effectuent une recherche vers l’avant ou vers l’arrière pour une chaîne de texte ou un attribut de texte correspondant unique. Ils doivent retourner la **valeur null** si aucune correspondance n’est trouvée.
-   La méthode [**ITextRangeProvider :: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) doit retourner l’adresse acquise à partir de la fonction [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) ou [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) si l’attribut associé varie dans la plage, ou si l’attribut n’est pas pris en charge par le contrôle de texte. La spécification du modèle de contrôle **TextRange** n’autorise pas l’ajout de nouveaux identificateurs d’attribut de texte ni la modification de la façon dont les attributs existants sont définis.
-   Si possible, la méthode [**ITextRangeProvider :: GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) doit retourner un tableau qui contient un rectangle englobant pour chaque ligne de texte complètement ou partiellement visible dans une plage de texte. Si ce n’est pas possible, le fournisseur peut retourner un tableau qui contient les rectangles englobants de lignes entièrement visibles uniquement ; Toutefois, cela limite la capacité d’une application cliente à décrire avec précision le mode de présentation du texte à l’écran.
-   La méthode [**ITextRangeProvider :: GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) doit retourner tous les éléments enfants incorporés dans une plage de texte, mais elle n’a pas besoin de retourner des enfants des éléments enfants. Par exemple, si une plage de texte contient une table qui a plusieurs cellules enfants, la méthode **GetChildren** peut retourner uniquement l’élément de table et non les éléments de cellule. Pour des raisons de performances ou d’architecture, un fournisseur peut ne pas être en mesure d’exposer tous les objets incorporés qui sont hébergés dans un document de l’arborescence Automation. Dans ce cas, le fournisseur doit au moins prendre en charge l’énumération d’objets enfants par le biais de la méthode **GetChildren** et, en guise d’option, prendre en charge le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) pour la prise en charge de la dévirtualisation.
-   La méthode [**ITextRangeProvider :: GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) retourne généralement le fournisseur de texte qui fournit la plage de texte. Toutefois, si le fournisseur de texte prend en charge des objets enfants tels que des tables ou des liens hypertexte, l’élément englobant peut être un descendant du fournisseur de texte. L’élément retourné par **GetEnclosingElement** doit être l’élément le plus proche de la plage de texte spécifiée. Par exemple, si la plage de texte se trouve dans une cellule d’une table, **GetEnclosingElement** doit retourner la cellule conteneur au lieu de l’élément de table.
-   La méthode [**ITextRangeProvider :: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) doit retourner le texte brut de la plage. Pour plus d’informations, consultez acquisition de texte à partir d’une plage de texte.
-   L’appel de [**ITextRangeProvider :: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) doit aligner le texte dans la fenêtre d’affichage du contrôle de texte comme spécifié par le paramètre *alignToTop* . Bien qu’il n’y ait aucune exigence en termes d’alignement horizontal, la plage de texte doit être visible à la fois horizontalement et verticalement. Lors de l’évaluation du paramètre *alignToTop* , un fournisseur doit prendre en compte l’orientation du contrôle Text et le sens du déroulement du texte. Par exemple, si *alignToTop* a la **valeur true** pour un contrôle de texte orienté verticalement contenant du texte qui se lit de droite à gauche, le fournisseur doit aligner la plage de texte sur le côté droit de la fenêtre d’affichage.
-   Lors du déplacement d’un document [**par \_ ligne TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si la plage de texte entre dans une table incorporée, chaque ligne de texte dans une cellule doit être traitée comme une ligne.

## <a name="required-members-for-itextprovider"></a>Membres requis pour **ITextProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) .



| Membres nécessaires                                                                                        | Type de membre | Notes |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Propriété    | None  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Propriété    | None  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Méthode      | None  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Méthode      | None  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Méthode      | None  |
| [**Telle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Méthode      | None  |
| [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)                   | Événement       | None  |
| [**\_TextSelectionChangedEventId de texte UIA \_**](uiauto-event-ids.md) | Événement       | None  |



 

Les propriétés et méthodes supplémentaires suivantes sont requises pour implémenter l’interface [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) .



| Membres nécessaires                                                         | Type de membre | Notes |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Méthode      | None  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Méthode      | None  |



 

## <a name="required-members-for-itextrangeprovider"></a>Membres requis pour **ITextRangeProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) .



| Membres nécessaires                                                                 | Type de membre | Notes |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Méthode      | None  |
| [**Clone**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Méthode      | None  |
| [**Comparer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Méthode      | None  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Méthode      | None  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Méthode      | None  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Méthode      | None  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Méthode      | None  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Méthode      | None  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Méthode      | None  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Méthode      | None  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Méthode      | None  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Méthode      | None  |
| [**Activer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Méthode      | None  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Méthode      | None  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Méthode      | None  |
| [**Sélectionner**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Méthode      | None  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Méthode      | None  |



 

Les propriétés et méthodes supplémentaires suivantes sont requises pour implémenter l’interface [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) .



| Membres nécessaires                                                      | Type de membre | Notes                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Méthode      | Consultez la section « implémentation de ShowContextMenu ». |



 

Le modèle de contrôle **TextRange** n’a pas d’événements associés.

## <a name="supporting-text-ranges"></a>Prise en charge des plages de texte

Cette section décrit comment un fournisseur doit implémenter différentes méthodes des interfaces [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) et [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) pour prendre en charge le modèle de contrôle **TextRange** .

### <a name="manipulating-a-text-range-by-text-unit"></a>Manipulation d’une plage de texte par unité de texte

L’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) fournit plusieurs méthodes pour manipuler et parcourir les plages de texte dans un contrôle textuel. Les méthodes [**ITextRangeProvider :: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)et [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) déplacent une plage de texte ou l’un de ses points de terminaison à l’aide de l’unité de texte spécifiée, telle que caractère, mot, paragraphe, et ainsi de suite. Pour plus d’informations, consultez [UI Automation Text Units](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

En dépit de son nom, la méthode [**ITextRangeProvider :: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) ne développe pas nécessairement une plage de texte. Au lieu de cela, il « normalise » une plage de texte en déplaçant les points de terminaison afin que la plage englobe l’unité de texte spécifiée. La plage est développée si elle est inférieure à l’unité spécifiée, ou réduite si elle est plus longue que l’unité spécifiée. Il est essentiel que la méthode **ExpandToEnclosingUnit** normalise toujours les plages de texte de manière cohérente ; dans le cas contraire, d’autres aspects de la manipulation de la plage de texte par unité de texte seraient imprévisibles. Le diagramme suivant montre comment **ExpandToEnclosingUnit** normalise une plage de texte en déplaçant les points de terminaison de la plage.

![Diagramme montrant les positions des points de terminaison de plage de texte avant et après un appel à ExpandToEnclosingUnit](images/expandtoenclosingunit.jpg)

Si la plage de texte commence au début d’une unité de texte et se termine au début de la limite d’unité de texte suivante, ou avant, le point de terminaison de fin est déplacé vers la limite d’unité de texte suivante (voir 1 et 2 dans le diagramme précédent).

Si la plage de texte commence au début d’une unité de texte et se termine à, ou après, la limite d’unité suivante, le point de terminaison de fin reste ou est déplacé vers la limite d’unité suivante après le point de terminaison de départ (voir 3 et 4 dans l’illustration précédente). S’il existe plusieurs limites d’unité de texte entre les points de terminaison de début et de fin, le point de terminaison de fin est déplacé vers la limite d’unité suivante après le point de terminaison de départ, ce qui a pour résultat une plage de texte d’une longueur d’une unité de texte.

Si la plage de texte commence au milieu de l’unité de texte, le point de terminaison de départ est déplacé vers le début de l’unité de texte, et le point de terminaison de fin est déplacé vers l’avant ou vers l’arrière, le cas échéant, vers la limite d’unité suivante après le point de terminaison de départ (voir 5 à 8 dans le schéma précédent).

Quand la méthode [**ITextRangeProvider :: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) est appelée, le fournisseur normalise la plage de texte par l’unité de texte spécifiée, en utilisant la même logique de normalisation que la méthode [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) . Ensuite, le fournisseur déplace la plage vers l’arrière ou vers l’avant par le nombre spécifié d’unités de texte. Lors du déplacement de la plage, le fournisseur doit ignorer les limites des objets incorporés dans le texte. (Toutefois, la limite d’unité elle-même peut être affectée par l’existence d’un objet incorporé). Le diagramme suivant montre comment la méthode **Move** déplace une plage de texte, Unit by Unit, sur des objets incorporés et des limites d’unité de texte.

![Diagramme montrant comment la méthode Move déplace les points de terminaison de plage entre les limites d’unités d’objet et de texte](images/move.jpg)

La méthode [**ITextRangeProvider :: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) déplace l’un des points de terminaison vers l’avant ou vers l’arrière selon l’unité de texte spécifiée, comme le montre l’illustration suivante.

![Diagramme montrant comment MoveEndpointByUnit déplace le point de terminaison d’une plage](images/moveendpointbyunit.gif)

La méthode [**ITextRangeProvider :: MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) permet à une application cliente de définir un point de terminaison d’une plage de texte au même emplacement que le point de terminaison spécifié d’une deuxième plage de texte.

### <a name="selecting-text-in-a-text-range"></a>Sélection de texte dans une plage de texte

L’interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) comprend plusieurs méthodes pour contrôler la sélection de texte dans un contrôle textuel.

La méthode [**ITextRangeProvider :: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) doit sélectionner le texte qui correspond à une plage de texte et supprimer la sélection précédente, le cas échéant, du contrôle de texte. Si **Select** est appelé sur une plage de texte dégénérée, le fournisseur doit déplacer le point d’insertion vers l’emplacement de la plage de texte sans sélectionner de texte.

Si un contrôle prend en charge la sélection de plusieurs étendues de texte disjointes, les méthodes [**ITextRangeProvider :: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) et [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) ajoutent des plages de texte à, et les suppriment de, la collection de plages de texte sélectionnées. Si le contrôle ne prend en charge qu’une plage de texte sélectionnée à la fois, mais que l’opération de sélection entraînerait la sélection de plusieurs plages de texte disjointes, le fournisseur doit retourner une erreur d' **E \_ INVALIDOPERATION** ou étendre ou tronquer la sélection actuelle. La propriété [**ITextProvider :: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) doit indiquer si un contrôle prend en charge la sélection d’une ou plusieurs étendues de texte, ou aucune.

Si un contrôle textuel prend en charge les insertions de texte, l’appel de [**ITextRangeProvider :: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) ou [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) sur une plage de texte dégénérée dans le contrôle doit déplacer le point d’insertion, mais ne doit pas sélectionner de texte.

### <a name="acquiring-text-from-a-text-range"></a>Acquisition de texte à partir d’une plage de texte

La méthode [**ITextRangeProvider :: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) doit retourner le texte brut d’une plage de texte. Le texte brut doit inclure tous les caractères de contrôle trouvés dans le texte source, tels que les retours chariot et la marque Unicode de gauche à droite (LRM). Le texte brut ne doit pas inclure de balises de balisage telles que du code HTML qui peuvent être présentes dans le texte source. En outre, tous les codes d’échappement du texte source doivent être convertis en équivalents en texte brut. Par exemple, " &nbsp; " doit être converti en un caractère d’espace simple.

Si un objet incorporé s’étend à une plage de texte, le texte brut doit inclure le texte interne de l’objet, mais pas le texte de remplacement (la propriété Name de l’objet incorporé), car il peut être incohérent avec le texte interne descriptif. Pour plus d’informations, consultez [Comment UI Automation expose des objets incorporés](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implémentation de ShowContextMenu

[**ITextRangeProvider2 :: ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) doit toujours afficher le menu contextuel au point de terminaison de début de la plage. Cela doit être équivalent à ce qui se passerait si l’utilisateur a appuyé sur la touche de menu contextuel ou MAJ + F10 avec le point d’insertion au début de la plage.

Si l’indication du menu contextuel entraîne généralement le déplacement du point d’insertion vers un emplacement donné, vous devez le faire pour appeler par programmation [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) pour la prise en charge d’UI Automation.

## <a name="interoperability-with-the-system-caret"></a>Interopérabilité avec le signe insertion du système

La prise en charge correcte du point d’insertion est essentielle pour de nombreuses applications clientes, notamment celles qui ne sont pas basées sur UI Automation. Dans le modèle de contrôle **Text** , le point d’insertion est représenté par une plage de texte dégénérée (vide) à la position du signe insertion du système. Lorsque le point d’insertion se déplace, un contrôle doit déclencher l’événement **TextSelectionChanged** ([**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)). Certaines applications clientes dépendent de cet événement pour surveiller l’emplacement du point d’insertion et pour effectuer le suivi de la sélection de texte.

Lorsqu’un contrôle contient du texte sélectionné, la conception actuelle du modèle de contrôle **Text** ne permet pas d’associer directement l’emplacement du point d’insertion à une plage de texte particulière. Le fournisseur doit effectuer le suivi de la sélection de texte et définir l’emplacement du point d’insertion de manière appropriée. Étant donné que la sélection de texte s’effectue généralement en déplaçant le point d’insertion tout en maintenant la touche Maj ou CTRL enfoncée, ou les deux, un fournisseur peut effectuer le suivi de la sélection de texte en vérifiant l’état de ces clés à chaque modification de la sélection.

Étant donné que l’infrastructure d’accessibilité offre une prise en charge intégrée du signe insertion du système mais pas d’un signe insertion personnalisé, les contrôles textuels doivent utiliser le signe insertion du système chaque fois que cela est possible. Les contrôles qui utilisent un signe insertion personnalisé peuvent garantir que le signe insertion est accessible en créant un signe insertion système qui a les mêmes dimensions que le signe insertion personnalisé et le positionnement du signe insertion système au même emplacement dans l’interface utilisateur du contrôle que le signe insertion personnalisé, c’est-à-dire au point d’insertion. En guise d’alternative, un contrôle qui utilise un signe insertion personnalisé peut implémenter un fournisseur Microsoft Active Accessibility pour le [**\_ signe insertion objid**](object-identifiers.md) pour fournir les informations d’accessibilité directement pour votre signe insertion personnalisé.

Pour plus d’informations sur le signe insertion du système, consultez les [signes](/windows/desktop/menurc/carets).

Pour tester si votre contrôle expose correctement l’emplacement du signe insertion du système, utilisez les outils [inspecter](inspect-objects.md) et [Observateur d’événements accessibles](accessible-event-watcher.md) .

Les coordonnées d’écran du centre de la bitmap du signe insertion du système doivent toujours correspondre à l’emplacement du point d’insertion. De cette façon, un client peut utiliser les coordonnées d’écran du signe insertion dans un appel à [**ITextProvider :: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) pour récupérer une plage de texte qui représente précisément l’emplacement du point d’insertion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Text (type de contrôle)](uiauto-supporttextcontroltype.md)
</dt> <dt>

[TextEdit (modèle de contrôle)](textedit-control-pattern.md)
</dt> <dt>

[Modèle de contrôle TextChild](textchild-control-pattern.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 