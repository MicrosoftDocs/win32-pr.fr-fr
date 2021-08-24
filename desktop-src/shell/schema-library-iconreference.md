---
description: L' <iconReference> élément spécifie une icône personnalisée pour cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs ni d’éléments enfants.
title: Élément iconReference (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 84e200fa4969dc376661bd32851296d80c74120939afc995754cb2937ea04be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820229"
---
# <a name="iconreference-element-library-schema"></a>Élément iconReference (schéma de bibliothèque)

L' <iconReference> élément spécifie une icône personnalisée pour cette bibliothèque. Cet élément est facultatif et n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants |
|------------------------------------------------------------------------------|----------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Remarques

La référence d’icône doit être spécifiée sous une forme appropriée pour la fonction [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) . Par exemple : `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Élément folderType (schéma de bibliothèque)](schema-library-foldertype.md)
</dt> <dt>

[Élément isLibraryPinned (schéma de bibliothèque)](schema-library-islibrarypinned.md)
</dt> <dt>

[Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md)
</dt> <dt>

[Élément Name (schéma de bibliothèque)](schema-library-name.md)
</dt> <dt>

[Élément ownerSID (schéma de bibliothèque)](schema-library-ownersid.md)
</dt> <dt>

[Élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md)
</dt> <dt>

[Élément searchConnectorDescription (schéma de bibliothèque)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Élément searchConnectorDescriptionList (schéma de bibliothèque)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Élément templateInfo (schéma de bibliothèque)](schema-library-templateinfo.md)
</dt> <dt>

[version, élément (schéma de bibliothèque)](schema-library-version.md)
</dt> </dl>

 

 



