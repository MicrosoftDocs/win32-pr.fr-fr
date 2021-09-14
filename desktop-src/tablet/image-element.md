---
description: Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Élément Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235086"
---
# <a name="image-element"></a>Élément Image

Contient des données binaires encodées pour une image dans le document Journal, le cas échéant.

## <a name="definition"></a>Définition

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Éléments parents

[**Humidité**](content-element--journal-reader.md)

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

[**Contexte**](background-element.md)
</dt> </dl>

 

 



