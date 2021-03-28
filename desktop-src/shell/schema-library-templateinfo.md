---
description: L' <templateInfo> élément est un conteneur pour l’élément FolderType, qui spécifie un type de dossier pour afficher les résultats d’une requête sur cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Élément templateInfo (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527304"
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

 

 
