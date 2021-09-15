---
description: L' &lt; &gt; élément Name spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Élément Name (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525368"
---
# <a name="name-element-library-schema"></a>Élément Name (schéma de bibliothèque)

L' &lt; &gt; élément Name spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants |
|------------------------------------------------------------------------------|----------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Notes

le nom est le nom de bibliothèque convivial qui s’affiche dans Windows Explorer. Le nom peut être spécifié dans un &lt; DllName &gt; , &lt; format d’index &gt; , comme dans l’exemple suivant.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
