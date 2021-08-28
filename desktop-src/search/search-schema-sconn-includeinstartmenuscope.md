---
description: l' &lt; élément includeInStartMenuScope booléen facultatif &gt; spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche menu Démarrer.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Élément includeInStartMenuScope (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20696dc6d2bc41b3f693e771a59541204e376e7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882386"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Élément includeInStartMenuScope (schéma du connecteur de recherche)

l' &lt; élément includeInStartMenuScope booléen facultatif &gt; spécifie si ce connecteur de recherche doit être inclus dans l’étendue de recherche menu Démarrer. La valeur par défaut est true pour les connecteurs de recherche utilisant le système de fichiers comme source de données, et false pour les connecteurs de recherche utilisés par les gestionnaires de propriétés. Cet élément n’a pas d’éléments enfants ni d’attributs.

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



 

## <a name="remarks"></a>Remarques

si vous incluez le connecteur de recherche dans l’étendue menu Démarrer, les utilisateurs peuvent rechercher votre emplacement dans la zone de recherche de la menu Démarrer.

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



