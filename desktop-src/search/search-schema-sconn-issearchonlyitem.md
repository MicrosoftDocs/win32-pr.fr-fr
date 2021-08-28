---
description: L' &lt; élément booléen isSearchOnlyItem &gt; spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Élément isSearchOnlyItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524a69198a650e0cb995d2ff8b4fc942ebfdaddc
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883412"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Élément isSearchOnlyItem (schéma du connecteur de recherche)

L' &lt; élément booléen isSearchOnlyItem &gt; spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.

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



 

## <a name="remarks"></a>Remarques

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



 

 



