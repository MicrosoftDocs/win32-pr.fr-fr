---
description: L' <dateCreated> élément facultatif identifie la date et l’heure de création de ce connecteur de recherche, à l’aide de la norme ISO 8601. Elle n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Élément dateCreated (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b59af62b2bd7ce8678fafb1fdd84646314f41a51414b4285db3077b5db0e0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944399"
---
# <a name="datecreated-element-search-connector-schema"></a>Élément dateCreated (schéma du connecteur de recherche)

L' <dateCreated> élément facultatif identifie la date et l’heure de création de ce connecteur de recherche, à l’aide de la norme ISO 8601. Elle n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
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

Le format de la valeur de cet élément suit la norme ISO 8601. Une utilisation courante est l’un des éléments suivants :

-   \[YYYY \] - \[ mm \] - \[ JJ \] T \[ hh \] : \[ mm \] : \[ SS \] ± \[ hh \] : \[ mm \] ("1981-04-05T14:30:30-05:00")
-   \[AAAA \] \[ mm \] \[ JJ \] T \[ hh \] \[ mm \] \[ SS \] Z (« 19810405T193030Z »)

## <a name="example"></a>Exemple


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



