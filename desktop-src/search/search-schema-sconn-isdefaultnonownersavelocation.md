---
description: L’élément booléen facultatif <isDefaultNonOwnerSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517236"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)

L’élément booléen facultatif <isDefaultNonOwnerSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Si la valeur est true, lorsqu’un utilisateur d’un autre ordinateur d’un groupe résidentiel choisit d’enregistrer un élément, l’Explorateur Windows l’enregistre à l’emplacement spécifié dans l' <simpleLocation> élément.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



