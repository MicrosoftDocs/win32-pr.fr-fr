---
description: L' <folderType> élément spécifie un GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe ; sinon, il est facultatif. Cet élément n’a pas d’attributs ni d’éléments enfants.
title: Élément folderType (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972302"
---
# <a name="foldertype-element-library-schema"></a>Élément folderType (schéma de bibliothèque)

L' <folderType> élément spécifie un GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe ; sinon, il est facultatif. Cet élément n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                           | Éléments enfants |
|--------------------------------------------------------------------------|----------------|
| [Élément templateInfo (schéma de bibliothèque)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Notes

La définition d’un type de dossier détermine les colonnes et les détails qui s’affichent dans l’Explorateur Windows par défaut. Les identificateurs de type de dossier ([**FOLDERTYPEID**](foldertypeid.md)) sont des GUID définis dans shlguid. h. Le tableau suivant répertorie les GUID des types de dossiers courants.



| Type de dossier      | GUID                                   |
|------------------|----------------------------------------|
| Bibliothèque générique  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Bibliothèques d’utilisateurs  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Dossier Documents | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Dossier images  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Dossier vidéos    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Dossier Games     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Dossier musique     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Contacts         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Élément iconReference (schéma de bibliothèque)](schema-library-iconreference.md)
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

 

 



