---
description: l’élément booléen facultatif <isIndexed> spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance à l’aide de Windows recherche 4 ou version ultérieure).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Élément isIndexed (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afcd1a95ec14b3bbea80374d8925a88231feb0110a421c2c850a297672d0c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711049"
---
# <a name="isindexed-element-search-connector-schema"></a>Élément isIndexed (schéma du connecteur de recherche)

l’élément booléen facultatif <isIndexed> spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance à l’aide de Windows recherche 4 ou version ultérieure). La valeur par défaut est true pour les dossiers locaux. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
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



 

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



