---
description: L' <isSearchOnlyItem> élément boolean spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Élément isSearchOnlyItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525455"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Élément isSearchOnlyItem (schéma du connecteur de recherche)

L' <isSearchOnlyItem> élément boolean spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Notes

La valeur `true` indique que les utilisateurs ne peuvent pas parcourir l’emplacement du connecteur de recherche. La valeur `false` indique que les utilisateurs peuvent parcourir l’emplacement du connecteur de recherche.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



