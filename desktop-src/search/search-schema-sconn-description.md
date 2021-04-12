---
description: Facultatif <description> élément spécifie une description pour ce connecteur de recherche. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Description, élément (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318145"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="939ec-105">Description, élément (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="939ec-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="939ec-106">Facultatif</span><span class="sxs-lookup"><span data-stu-id="939ec-106">The optional</span></span> <description> <span data-ttu-id="939ec-107">élément spécifie une description pour ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="939ec-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="939ec-108">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="939ec-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="939ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="939ec-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="939ec-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="939ec-110">Element Information</span></span>



| <span data-ttu-id="939ec-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="939ec-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="939ec-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="939ec-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="939ec-113">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="939ec-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="939ec-114">Notes</span><span class="sxs-lookup"><span data-stu-id="939ec-114">Remarks</span></span>

<span data-ttu-id="939ec-115">La description doit être conviviale, car elle peut être utilisée dans les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="939ec-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="939ec-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="939ec-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



