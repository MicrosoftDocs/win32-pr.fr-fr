---
description: L' <iconReference> élément facultatif spécifie une icône personnalisée pour cet emplacement. Cet élément n’a pas d’attributs ni d’éléments enfants.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Élément iconReference (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76391eb7079414abe13c4e45696ee3eacb3b968eb93b342b1b9e67825fac85c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862582"
---
# <a name="iconreference-element-search-connector-schema"></a>Élément iconReference (schéma du connecteur de recherche)

L' <iconReference> élément facultatif spécifie une icône personnalisée pour cet emplacement. Cet élément n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

Le format de la référence doit être spécifié sous une forme adaptée à la fonction [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (par exemple, <dll file name> , <icon index> ).

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
