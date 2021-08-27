---
description: L' &lt; élément propertyStore facultatif &gt; spécifie l’emplacement d’un IPropertyStore basé sur XML pour stocker les métadonnées ouvertes pour ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul élément enfant.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Élément propertyStore (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886798"
---
# <a name="propertystore-element-search-connector-schema"></a>Élément propertyStore (schéma du connecteur de recherche)

L' &lt; élément propertyStore facultatif &gt; spécifie l’emplacement d’un IPropertyStore basé sur XML pour stocker les métadonnées ouvertes pour ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul élément enfant.

## <a name="syntax"></a>Syntaxe


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [Élément Property de propertyStore (schéma du connecteur de recherche)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Exemple

L’exemple suivant montre un &lt; &gt; élément propertyStore avec deux &lt; éléments de propriété &gt; .


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



