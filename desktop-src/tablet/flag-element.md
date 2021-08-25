---
description: Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df40874178ba998ae9c864036b7befbf85179680de92cb68595f394e370e4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774079"
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

Aucun.

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------|
| Type d'élément | ComplexType [**FlagType**](flagtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk            |
| Nom du schéma  | Lecteur de journal                                        |



 

 

 



