---
description: L' <folderType> élément spécifie le GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe. Elle n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Élément folderType (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6b9d5682a85126a467c051b9f1103a4ac10f2f6936cc24dd4438a5f8c75d44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862598"
---
# <a name="foldertype-element-search-connector-schema"></a>Élément folderType (schéma du connecteur de recherche)

L' <folderType> élément spécifie le GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe. Elle n’a pas d’attributs ni d’éléments enfants.

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



 

 



