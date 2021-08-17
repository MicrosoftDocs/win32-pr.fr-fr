---
description: L' <name> élément spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Élément Name (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883939"
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



 

## <a name="remarks"></a>Remarques

le nom est le nom de bibliothèque convivial qui s’affiche dans Windows Explorer. Le nom peut être spécifié au <dllname> format, <index> comme dans l’exemple suivant.


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

 

 
