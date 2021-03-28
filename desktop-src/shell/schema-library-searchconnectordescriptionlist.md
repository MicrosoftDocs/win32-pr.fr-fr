---
description: Cet <searchConnectorDescriptionList> élément contient une liste de connecteurs de recherche qui correspondent aux emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par un <searchConnectorDescription> élément. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Élément searchConnectorDescriptionList (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973603"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Élément searchConnectorDescriptionList (schéma de bibliothèque)

Cet <searchConnectorDescriptionList> élément contient une liste de connecteurs de recherche qui correspondent aux emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par un <searchConnectorDescription> élément. Cet élément est facultatif et n’a pas d’attributs.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                               | Éléments enfants                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md) | [Élément searchConnectorDescription (schéma de bibliothèque)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Notes

Les connecteurs de recherche pour les étendues de recherche fédérée de Windows et de gestionnaire de protocole ne peuvent pas être inclus dans une bibliothèque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
