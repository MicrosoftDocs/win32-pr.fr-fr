---
description: L' <iconReference> élément facultatif spécifie une icône personnalisée pour cet emplacement. Cet élément n’a pas d’attributs ni d’éléments enfants.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Élément iconReference (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525462"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="27772-104">Élément iconReference (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="27772-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="27772-105">L' <iconReference> élément facultatif spécifie une icône personnalisée pour cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="27772-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="27772-106">Cet élément n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="27772-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="27772-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27772-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="27772-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="27772-108">Element Information</span></span>



| <span data-ttu-id="27772-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="27772-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="27772-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="27772-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="27772-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="27772-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="27772-112">Notes</span><span class="sxs-lookup"><span data-stu-id="27772-112">Remarks</span></span>

<span data-ttu-id="27772-113">Le format de la référence doit être spécifié sous une forme adaptée à la fonction [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (par exemple, <dll file name> , <icon index> ).</span><span class="sxs-lookup"><span data-stu-id="27772-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="27772-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="27772-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
