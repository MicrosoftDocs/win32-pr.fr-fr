---
description: Contient les informations textuelles de la note du journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235067"
---
# <a name="text-element"></a>Text, élément

Contient les informations textuelles de la note du journal.

## <a name="definition"></a>Définition

En cas d’utilisation avec le [**contenu**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Ou, en cas d’utilisation avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Éléments parents

[**Humidité**](content-element--journal-reader.md)

[**, Nœud**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs

Il n’existe aucun attribut lorsqu’il est utilisé avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md). Lorsqu’ils sont utilisés avec du [**contenu**](content-element--journal-reader.md), les attributs sont les suivants.



| Attribut  | Type                      | Obligatoire | Description                                                                             | Valeurs possibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément. | N’importe quel entier.              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.  | N’importe quel entier.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.                                          | Entier non négatif. |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.                                         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|   Élément           |   Valeur                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type d'élément | [**TextType**](texttype-complex-type.md) complexType (avec l’élément content) ou **XS : String** (avec les éléments [**, nœud**](groupnode-element.md) et [**TitleInfo**](titleinfo-element.md) ) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk<br/>                                                                                                                                               |
| Nom du schéma  | Lecteur de journal<br/>                                                                                                                                                                           |



 

 

 




