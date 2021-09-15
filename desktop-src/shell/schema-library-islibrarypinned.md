---
description: l' &lt; &gt; élément isLibraryPinned spécifie si cette bibliothèque est épinglée au volet de navigation dans Windows Explorer. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
title: Élément isLibraryPinned (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a535619fd38a0a557546f97f0a6ace64a065b61c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530393"
---
# <a name="islibrarypinned-element-library-schema"></a>Élément isLibraryPinned (schéma de bibliothèque)

l' &lt; &gt; élément isLibraryPinned spécifie si cette bibliothèque est épinglée au volet de navigation dans Windows Explorer. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants |
|------------------------------------------------------------------------------|----------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Notes

si la valeur est true, la bibliothèque est épinglée au volet de navigation de l’explorateur de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md)
</dt> <dt>

[Élément searchConnectorDescription (schéma de bibliothèque)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



