---
description: L' <imageLink> élément facultatif spécifie une miniature pour ce connecteur de recherche. Cet élément a un élément enfant obligatoire et aucun attribut.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Élément imageLink (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513188"
---
# <a name="imagelink-element-search-connector-schema"></a>Élément imageLink (schéma du connecteur de recherche)

L' <imageLink> élément facultatif spécifie une miniature pour ce connecteur de recherche. Cet élément a un élément enfant obligatoire et aucun attribut.

## <a name="syntax"></a>Syntaxe


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [Élément URL imageLink (schéma du connecteur de recherche)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Notes

La valeur imageLink peut être un chemin d’accès au système de fichiers local ou une URL. Le fichier image peut être l’un des types d’images de base pris en charge par Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Exemple d’élément imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



