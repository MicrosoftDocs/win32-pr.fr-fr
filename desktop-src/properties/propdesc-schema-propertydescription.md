---
description: Décrit une propriété canonique unique unique.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951605"
---
# <a name="propertydescription"></a><span data-ttu-id="9b15f-103">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9b15f-103">propertyDescription</span></span>

<span data-ttu-id="9b15f-104">Décrit une propriété canonique unique unique.</span><span class="sxs-lookup"><span data-stu-id="9b15f-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="9b15f-105">Chaque propriété de ce type destinée à être disponible dans le système doit avoir un élément [PropertyDescription]() correspondant.</span><span class="sxs-lookup"><span data-stu-id="9b15f-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="9b15f-106">Syntaxe pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b15f-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="9b15f-107">Syntaxe pour Vista</span><span class="sxs-lookup"><span data-stu-id="9b15f-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="9b15f-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9b15f-108">Element Information</span></span>



| <span data-ttu-id="9b15f-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="9b15f-109">Parent Element</span></span>                                                           | <span data-ttu-id="9b15f-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9b15f-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9b15f-111">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="9b15f-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="9b15f-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="9b15f-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="9b15f-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="9b15f-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="9b15f-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="9b15f-117">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="9b15f-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="9b15f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9b15f-118">Attributes</span></span>



| <span data-ttu-id="9b15f-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="9b15f-119">Attribute</span></span> | <span data-ttu-id="9b15f-120">Description</span><span class="sxs-lookup"><span data-stu-id="9b15f-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b15f-121">name</span><span class="sxs-lookup"><span data-stu-id="9b15f-121">name</span></span>      | <span data-ttu-id="9b15f-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b15f-122">Required.</span></span> <span data-ttu-id="9b15f-123">Nom de propriété canonique, unique au système ; par exemple, `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="9b15f-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="9b15f-124">Cette chaîne est de type canonique et est limitée à 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="9b15f-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="9b15f-125">Le nom respecte la casse et doit utiliser la syntaxe suivante : Publisher. application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="9b15f-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="9b15f-126">[**IPropertyDescription :: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) retourne cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9b15f-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="9b15f-127">IDFormat</span><span class="sxs-lookup"><span data-stu-id="9b15f-127">formatID</span></span>  | <span data-ttu-id="9b15f-128">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b15f-128">Required.</span></span> <span data-ttu-id="9b15f-129">Identificateur de format de la propriété (FMTID).</span><span class="sxs-lookup"><span data-stu-id="9b15f-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="9b15f-130">La valeur doit inclure des accolades englobantes ; par exemple, `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="9b15f-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="9b15f-131">[**IPropertyDescription :: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retourne cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9b15f-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="9b15f-132">propID</span><span class="sxs-lookup"><span data-stu-id="9b15f-132">propID</span></span>    | <span data-ttu-id="9b15f-133">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b15f-133">Required.</span></span> <span data-ttu-id="9b15f-134">Identificateur de propriété (PID); par exemple, `9` .</span><span class="sxs-lookup"><span data-stu-id="9b15f-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="9b15f-135">[**IPropertyDescription :: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retourne cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9b15f-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="9b15f-136">Cette valeur doit être supérieure ou égale à 2.</span><span class="sxs-lookup"><span data-stu-id="9b15f-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="9b15f-137">Les valeurs 0 et 1 sont réservées par le système.</span><span class="sxs-lookup"><span data-stu-id="9b15f-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
