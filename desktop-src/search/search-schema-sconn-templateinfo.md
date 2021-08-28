---
description: Cet &lt; élément templateInfo facultatif &gt; spécifie un type de dossier pour afficher les résultats d’une requête sur ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul enfant obligatoire.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Élément templateInfo (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880390"
---
# <a name="templateinfo-element-search-connector-schema"></a>Élément templateInfo (schéma du connecteur de recherche)

Cet &lt; élément templateInfo facultatif &gt; spécifie un type de dossier pour afficher les résultats d’une requête sur ce connecteur de recherche. Cet élément n’a pas d’attributs et un seul enfant obligatoire.

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



 

## <a name="remarks"></a>Remarques

si vous ne spécifiez pas un type de dossier particulier dans l' &lt; &gt; élément templateInfo, Windows utilise le type de dossier connecteur de recherche général {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Exemple d’élément templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



