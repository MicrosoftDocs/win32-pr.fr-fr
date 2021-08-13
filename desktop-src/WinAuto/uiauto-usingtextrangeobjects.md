---
title: Utilisation de plages de texte
description: Cette rubrique explique comment utiliser les propriétés et les méthodes de l’interface IUIAutomationTextRange pour accéder au contenu textuel d’un contrôle textuel et le manipuler.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- clients, utilisation d’objets de plage de texte
- contrôles textuels
- clients, plages de texte
- clients, modèle de contrôle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563984"
---
# <a name="using-text-ranges"></a>Utilisation de plages de texte

Cette rubrique explique comment utiliser les propriétés et les méthodes de l’interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) pour accéder au contenu textuel d’un contrôle textuel et le manipuler. Il contient les sections suivantes :

-   [Qu’est-ce qu’une plage de texte ?](#using-text-ranges)
-   [Acquisition d’objets de plage de texte](#acquiring-text-range-objects)
-   [Sélection de texte dans une plage de texte](#selecting-text-in-a-text-range)
-   [Récupération de texte à partir d’une plage de texte](#retrieving-text-from-a-text-range)
-   [Récupération des attributs de texte d’une plage de texte](#retrieving-text-attributes-from-a-text-range)
-   [Récupération d’objets incorporés à partir d’une plage de texte](#retrieving-embedded-objects-from-a-text-range)
-   [Manipulation d’une plage de texte](#manipulating-a-text-range)
-   [Défilement d’une plage de texte dans la vue](#scrolling-a-text-range-into-view)
-   [Récupération de l’élément englobant d’une plage de texte](#retrieving-the-enclosing-element-of-a-text-range)
-   [Comparaison et clonage de plages de texte](#comparing-and-cloning-text-ranges)
-   [Récupération des annotations](#retrieving-annotations)
    -   [Récupération de types d’annotations à partir d’une plage de texte](#retrieving-annotations-types-from-a-text-range)
    -   [Récupération de toutes les annotations d’une plage de texte](#retrieving-all-annotations-from-a-text-range)
    -   [Récupération d’informations sur une annotation particulière](#retrieving-information-about-a-particular-annotation)
    -   [Récupération du texte de la cible d’annotation](#retrieving-the-annotation-target-text)
-   [Récupération de styles visuels](#retrieving-visual-styles)
-   [Appel de menus contextuels à partir de plages de texte](#invoking-context-menus-from-text-ranges)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-a-text-range"></a>Qu’est-ce qu’une plage de texte ?

Le modèle d’objet de texte Microsoft UI Automation est basé sur le concept de la *plage de texte*. Une plage de texte est un objet qui expose l’interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) et représente une étendue contiguë de texte dans un contrôle textuel. Chaque plage de texte a à la fois un point de terminaison de départ et un point de terminaison de fin, et tout le contenu textuel entre les deux points de terminaison est considéré comme faisant partie de la plage. Une plage de texte dont le point de terminaison de départ et le point de terminaison de fin se trouvent au même emplacement est appelée une plage de texte *dégénérée* (ou vide). Une plage de texte dégénérée est utilisée pour marquer un emplacement spécifique dans le texte d’un contrôle, tel que l’emplacement du point d’insertion de texte.

## <a name="acquiring-text-range-objects"></a>Acquisition d’objets de plage de texte

Les applications clientes acquièrent des objets de plage de texte à l’aide des propriétés et des méthodes de l’interface [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) . La propriété [**IUIAutomationTextRangePattern ::D ocumentrange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) récupère une plage de texte qui représente l’intégralité du contenu textuel d’un contrôle textuel, tandis que d’autres méthodes acquièrent des plages de texte qui représentent une partie du contenu, telles que le texte sélectionné, le texte visible ou un objet incorporé dans le texte.

Les méthodes [**IUIAutomationTextRangePattern :: GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) et [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) peuvent récupérer des tableaux d’objets de plage de texte. Si un contrôle est partiellement masqué par une fenêtre ou un autre objet qui se chevauche, **GetVisibleRanges** retourne un tableau contenant un objet de plage de texte pour chaque ligne de texte partiellement visible. De même, si un contrôle textuel prend en charge la sélection de plusieurs étendues disjoint de texte, la fonction **GetSelection** retourne un tableau qui contient un objet plage de texte pour chaque étendue sélectionnée.

La méthode [**IUIAutomationTextRangePattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) permet à une application cliente de récupérer une plage de texte qui englobe un objet incorporé dans le contenu textuel. Le client spécifie le pointeur d’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) d’un objet incorporé, tel qu’une image, une table ou un lien hypertexte, et la méthode retourne une plage de texte qui englobe l’objet. Toutefois, si aucun texte n’est associé à l’objet incorporé, la méthode retourne une plage de texte dégénérée.

Une application cliente peut utiliser la méthode [**IUIAutomationTextRangePattern :: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) pour récupérer une plage de texte pour le texte visible ou l’objet incorporé qui est le plus proche des coordonnées d’écran spécifiées.

## <a name="selecting-text-in-a-text-range"></a>Sélection de texte dans une plage de texte

L’interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) comprend un certain nombre de méthodes qui permettent à une application cliente de contrôler la sélection de texte dans un contrôle textuel.

Les applications clientes peuvent utiliser la méthode [**IUIAutomationTextRange :: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) pour sélectionner le texte qui correspond à une plage de texte et pour supprimer la sélection précédente, le cas échéant, du contrôle de texte. L’appel de **Select** avec une plage de texte dégénérée déplace le point d’insertion vers l’emplacement de la plage de texte sans sélectionner de texte.

Si un contrôle prend en charge la sélection de plusieurs étendues de texte disjointes, un client peut utiliser les méthodes [**IUIAutomationTextRange :: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) et [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) pour ajouter des plages de texte à, et les supprimer de, la collection de plages de texte sélectionnées. Si le contrôle ne prend en charge qu’une seule plage de texte sélectionnée à la fois, mais que l’opération de sélection entraînerait la sélection de plusieurs plages de texte disjoint, la méthode retourne une erreur **E \_ INVALIDOPERATION** , ou étend ou tronque la sélection actuelle. Une application cliente peut déterminer si un contrôle prend en charge la sélection de plusieurs étendues de texte, ou aucune, en vérifiant la propriété [**IUIAutomationTextPattern :: SupportedTextSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection) .

Si un contrôle textuel prend en charge les insertions de texte, l’appel de [**IUIAutomationTextRange :: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) ou [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) sur une plage de texte dégénérée dans le contrôle déplace le point d’insertion, mais ne sélectionne aucun texte.

## <a name="retrieving-text-from-a-text-range"></a>Récupération de texte à partir d’une plage de texte

Les applications clientes peuvent utiliser la méthode [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) pour récupérer le texte brut d’une plage de texte. Le texte brut comprend tous les caractères de contrôle trouvés dans le texte source, tels que les retours chariot et la marque Unicode de gauche à droite (LRM). Le texte brut n’inclut pas de balises de balisage telles que du code HTML qui peuvent être présentes dans le texte source. En outre, les codes d’échappement du texte source sont convertis en équivalents en texte brut. Par exemple, « &nbsp; » est converti en un caractère d’espace simple.

Si un objet incorporé couvre une plage de texte, le texte brut comprend le texte interne de l’objet, mais pas le texte de remplacement (la propriété Name de l’objet incorporé). Pour plus d’informations, consultez [Comment UI Automation expose des objets incorporés](uiauto-textpattern-and-embedded-objects-overview.md).

La méthode [**IUIAutomationTextRange :: FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) recherche une chaîne particulière dans une plage de texte et, si elle est trouvée, retourne une nouvelle plage de texte qui englobe la chaîne.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Récupération des attributs de texte d’une plage de texte

Les attributs de texte déterminent le style de mise en forme du texte dans un contrôle textuel, et incluent des éléments tels que la couleur de premier plan, le style de puce, la taille de police, etc. UI Automation prend en charge un certain nombre d’attributs de texte et définit un identificateur pour chaque attribut pris en charge. Une application cliente peut interroger une plage de texte pour obtenir la valeur d’un attribut Text particulier en spécifiant un identificateur d’attribut dans un appel à la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) , ainsi qu’un pointeur vers une structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) qui reçoit la valeur de l’attribut. Pour obtenir des informations détaillées sur chaque attribut de texte pris en charge par UI Automation, consultez [identificateurs d’attribut de texte](uiauto-textattribute-ids.md).

La valeur récupérée par [**GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) représente la valeur de l’attribut dans l’ensemble de la plage de texte. Si tout le texte de la plage partage la même valeur pour l’attribut spécifié, cette valeur est retournée par **GetAttributeValue**. Toutefois, si la valeur de l’attribut varie dans la plage de texte, **GetAttributeValue** retourne un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) vers un objet de jeton statique appelé l’objet **ReservedMixedAttribute** . Pour déterminer si la valeur d’un attribut varie dans une plage de texte, une application cliente doit comparer les résultats de **GetAttributeValue** avec l’objet **ReservedMixedAttribute** récupéré à partir de la propriété [**IUIAutomation :: ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue) .

Un contrôle basé sur du texte n’est pas requis pour prendre en charge tous les attributs de texte UI Automation. Si un client appelle la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) et passe l’identificateur d’un attribut non pris en charge, la méthode retourne un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) vers un objet de jeton statique appelé l’objet **ReservedNotSupported** . Pour déterminer si un attribut particulier est pris en charge, une application cliente doit comparer les résultats de **GetAttributeValue** avec l’objet **ReservedNotSupported** récupéré à partir de la propriété [**IUIAutomation :: ReservedNotSupportedValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue) .

Les applications clientes peuvent utiliser la méthode [**IUIAutomationTextRange :: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) pour rechercher dans une plage de texte un texte qui a un attribut de texte particulier. S’il est trouvé, la méthode retourne une nouvelle plage de texte qui englobe le texte correspondant. Notez que **FindAttribute** retourne une plage de texte pour la correspondance de texte même si le texte n’est pas visible.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Récupération d’objets incorporés à partir d’une plage de texte

Une plage de texte peut inclure des objets incorporés, tels que des tables, des images, des liens hypertexte, etc. Une application cliente peut récupérer une collection de tous les objets incorporés dans une plage en appelant la méthode [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) . Les objets incorporés qui se chevauchent avec la plage mais qui ne sont pas entièrement inclus dans la collection sont également inclus dans la collection. Si la plage ne contient aucun objet incorporé, **GetChildren** récupère une collection vide.

Bien que cela dépende du fournisseur du contrôle textuel, la méthode [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) ne retourne généralement pas d’enfants des éléments incorporés. Par exemple, si une plage de texte contient une table comportant plusieurs cellules enfants, la méthode **GetChildren** retourne généralement simplement l’élément table et non les éléments Cell.

Pour des raisons de performances ou d’architecture, [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) peut ne pas être en mesure de récupérer les objets [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour tous les objets incorporés dans une plage de texte. Au lieu de cela, le fournisseur peut retourner une collection qui comprend des éléments virtualisés. Pour plus d’informations, consultez [utilisation d’éléments virtualisés](uiauto-workingwithvirtualizeditems.md).

## <a name="manipulating-a-text-range"></a>Manipulation d’une plage de texte

L’interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) fournit plusieurs méthodes pour manipuler et parcourir les plages de texte dans un contrôle textuel. Les méthodes [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)et [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) déplacent une plage de texte ou l’un de ses points de terminaison à l’aide de l’unité de texte spécifiée, telle que caractère, mot, paragraphe, et ainsi de suite. Pour plus d’informations, consultez [UI Automation Text Units](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

En dépit de son nom, la méthode [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) ne développe pas nécessairement une plage de texte. Au lieu de cela, il « normalise » une plage de texte en déplaçant les points de terminaison afin que la plage englobe exactement l’unité de texte spécifiée. La plage est développée si elle est inférieure à l’unité spécifiée, ou réduite si elle est plus longue que l’unité spécifiée. Le diagramme suivant montre comment **ExpandToEnclosingUnit** normalise une plage de texte en déplaçant les points de terminaison de la plage.

![Diagramme montrant les positions des points de terminaison avant et après un appel à ExpandToEnclosingUnit](images/expandtoenclosingunit.jpg)

Si la plage de texte commence au début d’une unité de texte et se termine au début de la limite d’unité de texte suivante, ou avant, le point de terminaison de fin est déplacé vers la limite d’unité de texte suivante (voir 1 et 2 dans l’illustration précédente).

Si la plage de texte commence au début d’une unité de texte et se termine à, ou après, la limite d’unité suivante, le point de terminaison de fin reste ou est déplacé vers la limite d’unité suivante après le point de terminaison de départ (voir 3 et 4 dans l’illustration précédente). S’il existe plusieurs limites d’unité de texte entre les points de terminaison de début et de fin, le point de terminaison de fin est déplacé vers la limite d’unité suivante après le point de terminaison de départ, ce qui a pour résultat une plage de texte d’une longueur d’une unité de texte.

Si la plage de texte commence au milieu d’une unité de texte, le point de terminaison de départ est déplacé vers le début de l’unité de texte, et le point de terminaison de fin est déplacé vers l’avant ou vers l’arrière, le cas échéant, vers la limite d’unité suivante après le point de terminaison de départ (voir 5 à 8 dans l’illustration précédente).

Lorsque la méthode [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) est appelée, le fournisseur normalise la plage de texte par l’unité de texte spécifiée. Ensuite, le fournisseur déplace la plage vers l’arrière ou vers l’avant par le nombre spécifié d’unités de texte. Lors du déplacement de la plage, le fournisseur ignore les limites des objets incorporés dans le texte. (Toutefois, la limite d’unité elle-même peut être affectée par l’existence d’un objet incorporé). Le diagramme suivant montre comment la méthode **Move** déplace une plage de texte, Unit by Unit, sur des objets incorporés et des limites d’unité de texte.

![Diagramme montrant comment la méthode Move déplace les points de terminaison de plage entre les limites d’unités d’objet et de texte](images/move.jpg)

La méthode [**IUIAutomationTextRange :: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) déplace l’un des points de terminaison vers l’avant ou vers l’arrière selon l’unité de texte spécifiée. L’illustration suivante montre comment un point de terminaison progresse.

![Diagramme montrant comment MoveEndpointByUnit déplace le point de terminaison d’une plage](images/moveendpointbyunit.gif)

La méthode [**IUIAutomationTextRange :: MoveEndpointByRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) permet à une application cliente de définir un point de terminaison d’une plage de texte au même emplacement que le point de terminaison spécifié d’une deuxième plage de texte.

## <a name="scrolling-a-text-range-into-view"></a>Défilement d’une plage de texte dans la vue

La méthode [**IUIAutomationTextRange :: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) fait défiler une plage de texte afin que le texte soit visible dans la fenêtre d’affichage du contrôle textuel. Lors de l’appel de **ScrollIntoView**, un client peut spécifier si le texte doit être aligné en haut ou en bas de la fenêtre d’affichage.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Récupération de l’élément englobant d’une plage de texte

Une application cliente peut utiliser la méthode [**IUIAutomationTextRange :: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) pour récupérer le pointeur d’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) de l’élément le plus profond qui englobe une plage de texte. L’élément englobant est généralement le fournisseur de texte qui fournit la plage de texte. Toutefois, si le fournisseur de texte prend en charge des éléments enfants tels que des tables ou des liens hypertexte, l’élément englobant peut être un descendant du fournisseur de texte.

## <a name="comparing-and-cloning-text-ranges"></a>Comparaison et clonage de plages de texte

L’interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) comprend deux méthodes pour comparer des plages de texte. La méthode [**IUIAutomationTextRange :: compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) compare les points de terminaison de début et de fin de deux plages de texte et retourne la **valeur true** si les deux points de terminaison sont identiques. La méthode **IUIAutomationTextRange :: CompareEndpoints** compare le point de terminaison de début ou de fin des deux plages. La valeur de retour est zéro si les points de terminaison sont identiques, ou une valeur positive ou négative qui indique les positions relatives des deux points de terminaison.

Les applications clientes peuvent utiliser la méthode [**IUIAutomationTextRange :: Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) pour créer une copie exacte de la plage de texte. La nouvelle plage de texte peut être manipulée indépendamment de la plage de texte d’origine.

## <a name="retrieving-annotations"></a>Récupération des annotations

Une plage de texte peut inclure des annotations si le contrôle textuel les prend en charge. Il existe de nombreux types d’annotations. Le fichier d’en-tête UIAutomationClient. h définit un ensemble de valeurs constantes nommées qui identifient les types d’annotations pris en charge par UI Automation. Pour plus d’informations, consultez [**identificateurs de type d’annotation**](uiauto-annotation-type-identifiers.md).

Certains genres d’annotations sont représentés par un élément Automation qui prend en charge le modèle de contrôle d' [annotation](uiauto-implementingannotation.md) (interface [**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) ). D’autres types d’annotations sont exposés par le biais du modèle de contrôle [TextRange](uiauto-about-text-and-textrange-patterns.md) . Par exemple, un fournisseur peut exposer un indicateur d’erreur orthographique simple en faisant en sorte que la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) renvoie un attribut de texte [**AnnotationTypes**](uiauto-textattribute-ids.md) de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)et une valeur null pour l’attribut de texte [**AnnotationObjects**](uiauto-textattribute-ids.md) .

### <a name="retrieving-annotations-types-from-a-text-range"></a>Récupération de types d’annotations à partir d’une plage de texte

Vous pouvez récupérer la liste des types d’annotations qui sont présents dans une plage de texte à l’aide de la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) . Lors de l’appel de la méthode, spécifiez un ID d’attribut de texte de [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) et un pointeur vers un paramètre de type [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant). Lorsque la méthode est retournée, le paramètre **Variant** contient une liste d’identificateurs de type d’annotation, un pour chaque type d’annotation dans la plage de texte. Pour plus d’informations, consultez [**identificateurs de type d’annotation**](uiauto-annotation-type-identifiers.md).

### <a name="retrieving-all-annotations-from-a-text-range"></a>Récupération de toutes les annotations d’une plage de texte

Pour récupérer les annotations d’une plage de texte, appelez la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) , en spécifiant un ID d’attribut de texte de [**UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) et un pointeur vers un paramètre de type [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant). Lorsque la méthode est retournée, le paramètre **Variant** contient une interface [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) qui représente un tableau d’éléments Automation, un pour chaque annotation dans la plage de texte. La propriété [**IUIAutomationElementArray :: length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) indique le nombre d’éléments dans le tableau, et la méthode [**IUIAutomationElementArray :: GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) récupère l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour un élément particulier.

### <a name="retrieving-information-about-a-particular-annotation"></a>Récupération d’informations sur une annotation particulière

Pour récupérer des informations sur une annotation particulière, récupérez d’abord l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour l’élément annotation, comme décrit dans la section précédente. Ensuite, récupérez l’interface [**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) pour l’annotation en appelant la méthode [**IUIAutomationElement :: GETCURRENTPATTERNAS**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) avec un ID de modèle de contrôle [**UIA \_ AnnotationPatternId**](uiauto-controlpattern-ids.md), un identificateur d’interface de IID \_ IUIAutomationAnnotationPattern et l’adresse d’une variable qui reçoit le pointeur **IUIAutomationAnnotation** pour l’annotation. Interrogez les propriétés de l’interface **IUIAutomationAnnotation** pour récupérer le nom du type et l’ID du type d’annotation, le nom de l’auteur de l’annotation, la date et l’heure de l’annotation et l’interface **IUIAutomationElement** pour l’élément qui est annoté.

### <a name="retrieving-the-annotation-target-text"></a>Récupération du texte de la cible d’annotation

En règle générale, une annotation s’applique à un sous-ensemble du texte d’une plage de texte. Après avoir récupéré l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour une annotation, vous pouvez passer l’interface à la méthode [**IUIAutomationTextRange2 :: RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) pour récupérer une plage de texte qui contient le texte qui est la cible de l’annotation.

## <a name="retrieving-visual-styles"></a>Récupération de styles visuels

Un fournisseur implémente le modèle de contrôle [styles](/windows/desktop/WinAuto/uiauto-implementingstyles) pour décrire un élément d’interface utilisateur doté d’un style, d’une couleur de remplissage, d’un motif de remplissage ou d’une forme spécifique. Cela s’avère particulièrement utile lors de la description d’éléments dans un document, qui ont souvent ces styles. Les styles comme celui-ci transmettent souvent des informations qui sont utiles pour les clients ayant des handicaps ; par exemple, les styles peuvent décrire une certaine chaîne comme titre d’un document ou un certain objet Flowchart comme un losange ou un cercle.

Vous pouvez utiliser la méthode [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) pour récupérer les noms et les identificateurs des styles visuels utilisés dans une plage de texte. Utilisez l’attribut de texte [**UIA \_ StyleNameAttributeId**](uiauto-textattribute-ids.md) pour récupérer les noms de style, et [**UIA \_ StyleIdAttributeId**](uiauto-textattribute-ids.md) pour récupérer les identificateurs de style.

Un contrôle basé sur du texte qui prend en charge les styles visuels peut implémenter le modèle de contrôle [styles](/windows/desktop/WinAuto/uiauto-implementingstyles) pour permettre aux clients d’accéder à des informations sur un style visuel utilisé par le contrôle. Les clients accèdent au modèle de contrôle styles par le biais de l’interface [**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) . Vous pouvez récupérer cette interface en appelant la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) ou [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) , en spécifiant [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) comme identificateur de modèle de contrôle.

L’interface [**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) comprend des propriétés et des méthodes qui fournissent les informations suivantes sur un style visuel :

-   Nom du style visuel, tel que « normal » ou « titre 1 ».
-   Identificateur du style visuel. Pour plus d’informations, consultez [**identificateurs de style**](uiauto-style-identifiers.md).
-   Couleur utilisée pour remplir le contrôle textuel.
-   Couleur du modèle utilisé pour remplir le contrôle textuel.
-   Forme du contrôle textuel.
-   Propriétés étendues ; autrement dit, une liste de noms et de valeurs de style spécifiques au contrôle.

## <a name="invoking-context-menus-from-text-ranges"></a>Appel de menus contextuels à partir de plages de texte

à partir de Windows 8.1, les plages de texte peuvent prendre en charge l’interface [**IUIAutomationTextRange2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) . Cette interface prend en charge la méthode [**ShowContextMenu**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) . Vous pouvez appeler cette méthode pour appeler n’importe quel menu contextuel associé à une plage de texte. Le scénario est la correction automatique des plages de texte ou la sélection d’un candidat IME. Dans ce cas, un menu contextuel s’affiche et prend en charge l’interaction de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de contrôle Text et TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 