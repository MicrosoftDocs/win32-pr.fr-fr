---
description: Conteneur pour un ou plusieurs éléments propertyDescription individuels.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524983"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="a7724-103">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="a7724-103">propertyDescriptionList</span></span>

<span data-ttu-id="a7724-104">Conteneur pour un ou plusieurs éléments [PropertyDescription](./propdesc-schema-propertydescription.md) individuels.</span><span class="sxs-lookup"><span data-stu-id="a7724-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="a7724-105">Un fichier de schéma de description de la propriété. propDesc doit contenir au moins un élément [propertyDescriptionList]() .</span><span class="sxs-lookup"><span data-stu-id="a7724-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7724-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7724-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a7724-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a7724-107">Element Information</span></span>



| <span data-ttu-id="a7724-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a7724-108">Parent Element</span></span>                        | <span data-ttu-id="a7724-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a7724-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a7724-110">schema</span><span class="sxs-lookup"><span data-stu-id="a7724-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="a7724-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a7724-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="a7724-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a7724-112">Attributes</span></span>



| <span data-ttu-id="a7724-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7724-113">Attribute</span></span> | <span data-ttu-id="a7724-114">Description</span><span class="sxs-lookup"><span data-stu-id="a7724-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="a7724-115">publisher</span><span class="sxs-lookup"><span data-stu-id="a7724-115">publisher</span></span> | <span data-ttu-id="a7724-116">Public.</span><span class="sxs-lookup"><span data-stu-id="a7724-116">Public.</span></span> <span data-ttu-id="a7724-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a7724-117">Required.</span></span> <span data-ttu-id="a7724-118">Nom complet du serveur de publication fournissant le schéma.</span><span class="sxs-lookup"><span data-stu-id="a7724-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="a7724-119">product</span><span class="sxs-lookup"><span data-stu-id="a7724-119">product</span></span>   | <span data-ttu-id="a7724-120">Public.</span><span class="sxs-lookup"><span data-stu-id="a7724-120">Public.</span></span> <span data-ttu-id="a7724-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a7724-121">Required.</span></span> <span data-ttu-id="a7724-122">Nom complet du produit qui fournit le schéma.</span><span class="sxs-lookup"><span data-stu-id="a7724-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="a7724-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a7724-123">Remarks</span></span>

<span data-ttu-id="a7724-124">Le [propertyDescriptionList]() ne doit pas être confondu avec les « listes de propriétés » et les [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), qui sont complètement distincts.</span><span class="sxs-lookup"><span data-stu-id="a7724-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
