---
description: L' <templateInfo> élément est un conteneur pour l’élément FolderType, qui spécifie un type de dossier pour afficher les résultats d’une requête sur cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Élément templateInfo (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda0c42e71db2e47335371b51d9dc819620e6b28dfac63ee9c0e2a640ccab0b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942089"
---
# <a name="templateinfo-element-library-schema"></a>Élément templateInfo (schéma de bibliothèque)

L' <templateInfo> élément est un conteneur pour l’élément [FolderType](schema-library-foldertype.md) , qui spécifie un type de dossier pour afficher les résultats d’une requête sur cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) | [Élément folderType (schéma de bibliothèque)](schema-library-foldertype.md)       |
|                                                                              | [Élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
