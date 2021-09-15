---
description: L' &lt; &gt; élément version spécifie la version de contenu de cette bibliothèque. Cet élément n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: version, élément (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1aeac399b5fa71b4a1ca57b63d8ecb95ede57f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412406"
---
# <a name="version-element-library-schema"></a>version, élément (schéma de bibliothèque)

L' &lt; &gt; élément version spécifie la version de contenu de cette bibliothèque. Cet élément n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants |
|------------------------------------------------------------------------------|----------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) | None           |



 

## <a name="remarks"></a>Notes

La version de contenu de la bibliothèque est différente de la version de format de fichier ( \* . Library-ms) de la bibliothèque. La version du format de fichier de la bibliothèque est spécifiée dans l' [espace de noms](library-schema-entry.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
