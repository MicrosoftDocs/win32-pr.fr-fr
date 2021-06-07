---
description: Contient un paragraphe.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Élément paragraph (Windows.ui.xaml.documents. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432231"
---
# <a name="paragraph-element"></a>Élément paragraph

Contient un paragraphe.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**Humidité**](content-element--journal-reader.md)

[**, Nœud**](groupnode-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Spline**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Attributs



| Attribut       | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**         | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**       | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height**      | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |
| **BlockNumber** | **xs:nonNegativeInteger** | Obligatoire | Numéro de bloc.                                                                           | Entier non négatif. |
| **LineNumber**  | **xs:nonNegativeInteger** | Obligatoire | Ligne sur laquelle le paragraphe commence.                                                 | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-----------------------------------------------------------------|
| Type d'élément | ComplexType [**ParagraphType**](paragraphtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                      |
| Nom du schéma  | Lecteur de journal                                                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Windows.ui.xaml.documents. h</dt> </dl> |



 

 




