---
description: L’élément booléen facultatif <includeInStartMenuScope> spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Élément includeInStartMenuScope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531652"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Élément includeInStartMenuScope (schéma du connecteur de recherche)

L’élément booléen facultatif <includeInStartMenuScope> spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche du menu Démarrer. La valeur par défaut est true pour les connecteurs de recherche utilisant le système de fichiers comme source de données, et false pour les connecteurs de recherche utilisés par les gestionnaires de propriétés. Cet élément n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
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

Si vous incluez le connecteur de recherche dans l’étendue du menu Démarrer, les utilisateurs peuvent effectuer une recherche dans votre emplacement à partir de la zone de recherche dans le menu Démarrer.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



