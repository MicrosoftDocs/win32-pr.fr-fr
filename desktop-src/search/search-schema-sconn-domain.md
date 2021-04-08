---
description: L' <domain> élément facultatif spécifie l’URL du service de recherche utilisé par ce connecteur de recherche. Il s’affiche dans le volet d’informations. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Élément de domaine (schéma de connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862146"
---
# <a name="domain-element-search-connector-schema"></a>Élément de domaine (schéma de connecteur de recherche)

L' <domain> élément facultatif spécifie l’URL du service de recherche utilisé par ce connecteur de recherche. Il s’affiche dans le volet d’informations. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

L’URL doit être le domaine de niveau supérieur pour le moteur de recherche. Par exemple : https://www.example.com.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



