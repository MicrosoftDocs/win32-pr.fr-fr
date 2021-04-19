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
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="dba99-104">Élément templateInfo (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="dba99-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="dba99-105">Cet <templateInfo> élément facultatif spécifie un type de dossier pour afficher les résultats d’une requête sur ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="dba99-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="dba99-106">Cet élément n’a pas d’attributs et un seul enfant obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dba99-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba99-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dba99-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="dba99-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dba99-108">Element Information</span></span>



| <span data-ttu-id="dba99-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dba99-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="dba99-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dba99-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="dba99-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="dba99-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="dba99-112">Élément folderType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="dba99-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="dba99-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dba99-113">Remarks</span></span>

<span data-ttu-id="dba99-114">Si vous ne spécifiez pas un type de dossier particulier dans l' <templateInfo> élément, Windows utilise le type de dossier connecteur de recherche général {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span><span class="sxs-lookup"><span data-stu-id="dba99-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="dba99-115">Exemple d’élément templateInfo</span><span class="sxs-lookup"><span data-stu-id="dba99-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



