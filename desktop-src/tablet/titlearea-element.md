---
description: Contient l’emplacement et les informations liées au titre de la note, le cas échéant.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Élément partie titlearea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f95c06e6aabe7c73cdc02a7fdb66c60f220adfbe72ea565b73cbc2c3f1a88bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589309"
---
# <a name="titlearea-element"></a>Élément partie titlearea

Contient l’emplacement et les informations liées au titre de la note, le cas échéant.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**Titre**](title-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|   Élément    | Valeur                                                           |
|--------------|-----------------------------------------------------------------|
| Type d'élément | ComplexType [**TitleAreaType**](titleareatype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                      |
| Nom du schéma  | Lecteur de journal                                                  |



 

 

 



