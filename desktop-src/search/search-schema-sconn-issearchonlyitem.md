---
description: L' <isSearchOnlyItem> élément boolean spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche. Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Élément isSearchOnlyItem (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525455"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="46c4e-104">Élément isSearchOnlyItem (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="46c4e-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="46c4e-105">L' <isSearchOnlyItem> élément boolean spécifie si le moteur de recherche prend en charge le mode de navigation en plus du mode de recherche.</span><span class="sxs-lookup"><span data-stu-id="46c4e-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="46c4e-106">Cet élément est facultatif et n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="46c4e-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c4e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46c4e-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="46c4e-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="46c4e-108">Element Information</span></span>



| <span data-ttu-id="46c4e-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="46c4e-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="46c4e-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46c4e-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="46c4e-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="46c4e-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="46c4e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="46c4e-112">Remarks</span></span>

<span data-ttu-id="46c4e-113">La valeur `true` indique que les utilisateurs ne peuvent pas parcourir l’emplacement du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="46c4e-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="46c4e-114">La valeur `false` indique que les utilisateurs peuvent parcourir l’emplacement du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="46c4e-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="46c4e-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="46c4e-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



