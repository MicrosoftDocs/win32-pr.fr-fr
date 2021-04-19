---
description: Cet <templateInfo> élément facultatif spécifie un type de dossier pour afficher les résultats d’une requête sur ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul enfant obligatoire.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Élément templateInfo (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516618"
---
# <a name="templateinfo-element-search-connector-schema"></a>Élément templateInfo (schéma du connecteur de recherche)

Cet <templateInfo> élément facultatif spécifie un type de dossier pour afficher les résultats d’une requête sur ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul enfant obligatoire.

## <a name="syntax"></a>Syntaxe


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                                                   | Éléments enfants                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Élément searchConnectorDescriptionType (schéma du connecteur de recherche)](search-schema-searchconnectordescription.md) | [Élément folderType (schéma du connecteur de recherche)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Notes

Si vous ne spécifiez pas un type de dossier particulier dans l' <templateInfo> élément, Windows utilise le type de dossier connecteur de recherche général {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Exemple d’élément templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



