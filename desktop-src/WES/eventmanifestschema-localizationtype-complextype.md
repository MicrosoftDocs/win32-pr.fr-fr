---
title: Type complexe LocalizationType
description: Définit un groupe de ressources localisées que vous référencez dans votre manifeste. | Type complexe LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType type complexe EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531483"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="f0863-105">Type complexe LocalizationType</span><span class="sxs-lookup"><span data-stu-id="f0863-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="f0863-106">Définit un groupe de ressources localisées que vous référencez dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="f0863-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f0863-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f0863-107">Child elements</span></span>



| <span data-ttu-id="f0863-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f0863-108">Element</span></span>                                                                         | <span data-ttu-id="f0863-109">Type</span><span class="sxs-lookup"><span data-stu-id="f0863-109">Type</span></span>                                                                       | <span data-ttu-id="f0863-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0863-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0863-111">**situées**</span><span class="sxs-lookup"><span data-stu-id="f0863-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="f0863-112">Définit un groupe de tables de chaînes qui contiennent les chaînes localisées que vous référencez dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="f0863-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="f0863-113">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="f0863-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="f0863-114">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="f0863-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="f0863-115">Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="f0863-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="f0863-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="f0863-116">Attributes</span></span>



| <span data-ttu-id="f0863-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f0863-117">Name</span></span>            | <span data-ttu-id="f0863-118">Type</span><span class="sxs-lookup"><span data-stu-id="f0863-118">Type</span></span>   | <span data-ttu-id="f0863-119">Description</span><span class="sxs-lookup"><span data-stu-id="f0863-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0863-120">culture</span><span class="sxs-lookup"><span data-stu-id="f0863-120">culture</span></span>         | <span data-ttu-id="f0863-121">string</span><span class="sxs-lookup"><span data-stu-id="f0863-121">string</span></span> | <span data-ttu-id="f0863-122">Nom de langage qui identifie la culture des chaînes localisées dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="f0863-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="f0863-123">Par exemple, « en-US » pour l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="f0863-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="f0863-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="f0863-124">fallbackCulture</span></span> | <span data-ttu-id="f0863-125">string</span><span class="sxs-lookup"><span data-stu-id="f0863-125">string</span></span> | <span data-ttu-id="f0863-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f0863-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="f0863-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0863-127">Requirements</span></span>



| <span data-ttu-id="f0863-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0863-128">Requirement</span></span> | <span data-ttu-id="f0863-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0863-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0863-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0863-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0863-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0863-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0863-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0863-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0863-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0863-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





