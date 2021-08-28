---
description: L' &lt; &gt; élément FolderType spécifie le GUID pour le type de dossier. Cet élément est obligatoire si l' &lt; &gt; élément templateInfo existe. Elle n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Élément folderType (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b693a1ff7007e6d63e108d16abe77ee421b3821a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882470"
---
# <a name="foldertype-element-search-connector-schema"></a>Élément folderType (schéma du connecteur de recherche)

L' &lt; &gt; élément FolderType spécifie le GUID pour le type de dossier. Cet élément est obligatoire si l' &lt; &gt; élément templateInfo existe. Elle n’a pas d’attributs ni d’éléments enfants.

## <a name="syntax"></a>Syntaxe


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                         | Éléments enfants |
|----------------------------------------------------------------------------------------|----------------|
| [Élément templateInfo (schéma du connecteur de recherche)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Remarques

le GUID par défaut est {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un type de dossier général pour les connecteurs de recherche fédérée (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Exemple d’élément folderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



