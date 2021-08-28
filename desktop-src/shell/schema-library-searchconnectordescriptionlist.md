---
description: Cet &lt; &gt; élément searchConnectorDescriptionList contient une liste de connecteurs de recherche mappés à des emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par &lt; un &gt; élément searchConnectorDescription. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Élément searchConnectorDescriptionList (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885605"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Élément searchConnectorDescriptionList (schéma de bibliothèque)

Cet &lt; &gt; élément searchConnectorDescriptionList contient une liste de connecteurs de recherche mappés à des emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par &lt; un &gt; élément searchConnectorDescription. Cet élément est facultatif et n’a pas d’attributs.

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

 

 
