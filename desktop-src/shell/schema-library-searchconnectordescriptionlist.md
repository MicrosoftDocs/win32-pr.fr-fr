---
description: Cet <searchConnectorDescriptionList> élément contient une liste de connecteurs de recherche qui correspondent aux emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par un <searchConnectorDescription> élément. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Élément searchConnectorDescriptionList (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9298ec0f25554f6e1b1ceb570630cf6e41c11fb027c2b1bb5496c8acc68ee41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111179"
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



 

## <a name="remarks"></a>Remarques

les connecteurs de recherche pour Windows des étendues de recherche fédérée et de gestionnaire de protocole ne peuvent pas être inclus dans une bibliothèque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
