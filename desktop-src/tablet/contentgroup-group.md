---
description: Définit un groupe qui contient un ensemble de contenu groupé dans une note de journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Groupe ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0085cc52a8fc29d3a51f4d1e1c8f42128b63db9e166a7a1c436dc15bff70a36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009009"
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

[**Dessin**](drawing-element.md)

[**Financière**](text-element.md)

[**Image**](docimage-element.md)

[**Activé**](flag-element.md)

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.<br/> | N’importe quel entier.<br/>              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.<br/>  | N’importe quel entier.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.<br/>                                          | Entier non négatif.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.<br/>                                         | Entier non négatif.<br/> |



 

## <a name="type-information"></a>Informations de type



|  Élément     | Valeur                                                     |
|-------------|--------------------------------------------|
| Espace de noms   | urn : schemas-microsoft-com : TabletPC : RichInk |
| Nom du schéma | Lecteur de journal                             |



 

 

 




