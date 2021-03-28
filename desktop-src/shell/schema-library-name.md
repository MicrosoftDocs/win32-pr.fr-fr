---
description: L' <name> élément spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Élément Name (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991812"
---
# <a name="name-element-library-schema"></a>Élément Name (schéma de bibliothèque)

L' <name> élément spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.

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

Le nom est le nom de bibliothèque convivial qui s’affiche dans l’Explorateur Windows. Le nom peut être spécifié au <dllname> format, <index> comme dans l’exemple suivant.


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

 

 
