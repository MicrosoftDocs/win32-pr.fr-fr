---
description: Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Groupe ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034874"
---
# <a name="contentgroup-group"></a>Groupe ContentGroup

Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.

## <a name="definition"></a>Définition

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Éléments enfants

[**, Nœud**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Schéma**](drawing-element.md)

[**Texte**](text-element.md)

[**Image**](docimage-element.md)

[**Indicateur**](flag-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.<br/> | N’importe quel entier.<br/>              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.<br/>  | N’importe quel entier.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.<br/>                                          | Entier non négatif.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.<br/>                                         | Entier non négatif.<br/> |



 

## <a name="type-information"></a>Informations de type



|             |                                            |
|-------------|--------------------------------------------|
| Espace de noms   | urn : schemas-microsoft-com : TabletPC : RichInk |
| Nom du schéma | Lecteur de journal                             |



 

 

 




