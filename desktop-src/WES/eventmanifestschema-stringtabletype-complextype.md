---
title: Type complexe StringTableType
description: Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste. | Type complexe StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType type complexe EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522540"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="68ef5-105">Type complexe StringTableType</span><span class="sxs-lookup"><span data-stu-id="68ef5-105">StringTableType Complex Type</span></span>

<span data-ttu-id="68ef5-106">Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="68ef5-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="68ef5-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="68ef5-107">Child elements</span></span>



| <span data-ttu-id="68ef5-108">Élément</span><span class="sxs-lookup"><span data-stu-id="68ef5-108">Element</span></span>                                                              | <span data-ttu-id="68ef5-109">Type</span><span class="sxs-lookup"><span data-stu-id="68ef5-109">Type</span></span> | <span data-ttu-id="68ef5-110">Description</span><span class="sxs-lookup"><span data-stu-id="68ef5-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="68ef5-111">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ef5-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="68ef5-112">Définit une chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="68ef5-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="68ef5-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="68ef5-113">Attributes</span></span>



| <span data-ttu-id="68ef5-114">Nom</span><span class="sxs-lookup"><span data-stu-id="68ef5-114">Name</span></span>       | <span data-ttu-id="68ef5-115">Type</span><span class="sxs-lookup"><span data-stu-id="68ef5-115">Type</span></span>   | <span data-ttu-id="68ef5-116">Description</span><span class="sxs-lookup"><span data-stu-id="68ef5-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ef5-117">id</span><span class="sxs-lookup"><span data-stu-id="68ef5-117">id</span></span>         | <span data-ttu-id="68ef5-118">string</span><span class="sxs-lookup"><span data-stu-id="68ef5-118">string</span></span> | <span data-ttu-id="68ef5-119">Identificateur qui identifie de façon unique la chaîne dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="68ef5-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="68ef5-120">Par exemple, « Printer. Connection ».</span><span class="sxs-lookup"><span data-stu-id="68ef5-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="68ef5-121">stringType</span><span class="sxs-lookup"><span data-stu-id="68ef5-121">stringType</span></span> | <span data-ttu-id="68ef5-122">string</span><span class="sxs-lookup"><span data-stu-id="68ef5-122">string</span></span> | <span data-ttu-id="68ef5-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="68ef5-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="68ef5-124">value</span><span class="sxs-lookup"><span data-stu-id="68ef5-124">value</span></span>      | <span data-ttu-id="68ef5-125">string</span><span class="sxs-lookup"><span data-stu-id="68ef5-125">string</span></span> | <span data-ttu-id="68ef5-126">La chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="68ef5-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="68ef5-127">Notes</span><span class="sxs-lookup"><span data-stu-id="68ef5-127">Remarks</span></span>

<span data-ttu-id="68ef5-128">Vous pouvez référencer les chaînes à partir de n’importe quel type de manifeste contenant l’attribut de message.</span><span class="sxs-lookup"><span data-stu-id="68ef5-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="68ef5-129">Pour faire référence à une chaîne avec un stringType « String » et un ID « Printer. Connection », utilisez $ (String. Printer. Connection) comme valeur de l’attribut de message.</span><span class="sxs-lookup"><span data-stu-id="68ef5-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ef5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68ef5-130">Requirements</span></span>



| <span data-ttu-id="68ef5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68ef5-131">Requirement</span></span> | <span data-ttu-id="68ef5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="68ef5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68ef5-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68ef5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="68ef5-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68ef5-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68ef5-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68ef5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="68ef5-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68ef5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





