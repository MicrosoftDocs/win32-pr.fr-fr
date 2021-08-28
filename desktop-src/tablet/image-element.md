---
description: Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Élément Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b1cfd62dd6c2f58c2c1da26f0a9564b8c070f5c57fdccc870fa8b52b3f37c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939832"
---
# <a name="image-element"></a>Élément Image

Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.

## <a name="definition"></a>Définition

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
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
|--------------|---------------------------------------------------------|
| Type d'élément | ComplexType [**ImageType**](imagetype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk              |
| Nom du schéma  | Lecteur de journal                                          |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Arrière-plan**](background-element.md)
</dt> </dl>

 

 



