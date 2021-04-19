---
description: L' <folderType> élément spécifie le GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe. Elle n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Élément folderType (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484401"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="6dee4-105">Élément folderType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="6dee4-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="6dee4-106">L' <folderType> élément spécifie le GUID pour le type de dossier.</span><span class="sxs-lookup"><span data-stu-id="6dee4-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="6dee4-107">Cet élément est obligatoire si l' <templateInfo> élément existe.</span><span class="sxs-lookup"><span data-stu-id="6dee4-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="6dee4-108">Elle n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="6dee4-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dee4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dee4-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6dee4-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6dee4-110">Element Information</span></span>



| <span data-ttu-id="6dee4-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="6dee4-111">Parent Element</span></span>                                                                         | <span data-ttu-id="6dee4-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6dee4-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6dee4-113">Élément templateInfo (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="6dee4-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6dee4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6dee4-114">Remarks</span></span>

<span data-ttu-id="6dee4-115">Le GUID par défaut est {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un type de dossier général pour les connecteurs de recherche fédérée (OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="6dee4-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="6dee4-116">Exemple d’élément folderType</span><span class="sxs-lookup"><span data-stu-id="6dee4-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



