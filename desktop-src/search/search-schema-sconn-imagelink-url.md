---
description: L' <url> élément spécifie une URL vers la miniature pour ce connecteur de recherche. Si <imageLink> existe, cet élément est obligatoire. Elle n’a pas d’éléments enfants ni d’attributs.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Élément URL imageLink (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513365"
---
# <a name="imagelink-url-element-search-connector-schema"></a>Élément URL imageLink (schéma du connecteur de recherche)

L' <url> élément spécifie une URL vers la miniature pour ce connecteur de recherche. Si <imageLink> existe, cet élément est obligatoire. Elle n’a pas d’éléments enfants ni d’attributs.

## <a name="syntax"></a>Syntaxe


```
<!-- url -->
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



| Élément parent                                                                   | Éléments enfants |
|----------------------------------------------------------------------------------|----------------|
| [Élément imageLink (schéma du connecteur de recherche)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Notes

La valeur peut être un chemin d’accès au système de fichiers local ou une URL. Le fichier image peut être l’un des types d’images de base pris en charge par Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Exemple d’élément imageLinkurl


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



