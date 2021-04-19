---
description: Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536973"
---
# <a name="flag-element"></a>Flag, élément

Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**Content**](content-element--journal-reader.md)

[**, Nœud**](groupnode-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                       |
|--------------|-------------------------------------------------------|
| Type d'élément | ComplexType [**FlagType**](flagtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk            |
| Nom du schéma  | Lecteur de journal                                        |



 

 

 



