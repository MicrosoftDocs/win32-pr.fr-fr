---
description: L' <simpleLocation> élément spécifie l’emplacement des connecteurs de recherche qui sont basés sur un système de fichiers ou un gestionnaire de protocole. Cet élément a deux éléments enfants et aucun attribut.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Élément simpleLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862460"
---
# <a name="simplelocation-element-search-connector-schema"></a>Élément simpleLocation (schéma du connecteur de recherche)

L' <simpleLocation> élément spécifie l’emplacement des connecteurs de recherche qui sont basés sur un système de fichiers ou un gestionnaire de protocole. Cet élément a deux éléments enfants et aucun attribut.

## <a name="syntax"></a>Syntaxe


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [Élément URL simpleLocation (schéma du connecteur de recherche)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | sérialisé : cet élément contient les ShellLink encodés en base64 pointant vers l’emplacement défini dans l' <url> élément. Windows 7 crée le ShellLink à partir de la valeur de l' <url> élément et met à jour correctement ce champ sur la première charge de cette bibliothèque. il doit donc rester vide par l’auteur. |



 

## <a name="remarks"></a>Remarques

Cet élément peut être utilisé à la place de <locationProvider> lorsque l’emplacement est sur le système de fichiers ou que le connecteur est un gestionnaire de protocole connu (comme MAPI :). Si <simpleLocation> est présent, il ne doit pas s’agir d’un <locationProvider> élément. Pour les connecteurs de recherche de fournisseur de services Web, utilisez à la [<locationProvider>](search-schema-sconn-locationprovider.md) place l’élément.

## <a name="examples"></a>Exemples


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



