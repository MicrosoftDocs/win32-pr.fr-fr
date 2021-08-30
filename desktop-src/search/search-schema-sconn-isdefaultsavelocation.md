---
description: L' &lt; élément IsDefaultSaveLocation booléen facultatif &gt; spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Élément isDefaultSaveLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a17324f7658290c0eed9345f899f0d9c94f208
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881902"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Élément isDefaultSaveLocation (schéma du connecteur de recherche)

L' &lt; élément IsDefaultSaveLocation booléen facultatif &gt; spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

quand un utilisateur choisit d’enregistrer un élément, Windows Explorer l’enregistre à l’emplacement spécifié dans l' &lt; élément simpleLocation &gt; . Les utilisateurs peuvent modifier ce paramètre à l’aide de la boîte de dialogue Propriétés du connecteur de recherche.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



