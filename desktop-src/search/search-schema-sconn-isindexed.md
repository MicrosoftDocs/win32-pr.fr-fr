---
description: l' &lt; élément isIndexed booléen facultatif &gt; spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance, à l’aide de Windows recherche 4 ou version ultérieure).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Élément isIndexed (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881848"
---
# <a name="isindexed-element-search-connector-schema"></a>Élément isIndexed (schéma du connecteur de recherche)

l' &lt; élément isIndexed booléen facultatif &gt; spécifie si l’emplacement décrit par le connecteur de recherche est indexé (localement ou à distance, à l’aide de Windows recherche 4 ou version ultérieure). La valeur par défaut est true pour les dossiers locaux. Cet élément n’a pas d’éléments enfants ni d’attributs.

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



 

 



