---
title: Élément Resources (LocalizationType)
description: Définit un groupe de tables de chaînes qui contiennent les chaînes localisées que vous référencez dans votre manifeste.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- élément Resources EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511535"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="50b72-104">Élément Resources (LocalizationType)</span><span class="sxs-lookup"><span data-stu-id="50b72-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="50b72-105">Définit un groupe de tables de chaînes qui contiennent les chaînes localisées que vous référencez dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="50b72-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="50b72-106">L’élément **Resources** est défini par le type complexe [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="50b72-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="50b72-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="50b72-107">Child elements</span></span>



| <span data-ttu-id="50b72-108">Élément</span><span class="sxs-lookup"><span data-stu-id="50b72-108">Element</span></span>                                                                  | <span data-ttu-id="50b72-109">Type</span><span class="sxs-lookup"><span data-stu-id="50b72-109">Type</span></span>                                                                       | <span data-ttu-id="50b72-110">Description</span><span class="sxs-lookup"><span data-stu-id="50b72-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="50b72-111">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="50b72-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="50b72-112">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="50b72-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="50b72-113">Définit une liste de chaînes localisées que vous pouvez référencer dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="50b72-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="50b72-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="50b72-114">Attributes</span></span>



| <span data-ttu-id="50b72-115">Nom</span><span class="sxs-lookup"><span data-stu-id="50b72-115">Name</span></span>    | <span data-ttu-id="50b72-116">Type</span><span class="sxs-lookup"><span data-stu-id="50b72-116">Type</span></span>   | <span data-ttu-id="50b72-117">Description</span><span class="sxs-lookup"><span data-stu-id="50b72-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b72-118">culture</span><span class="sxs-lookup"><span data-stu-id="50b72-118">culture</span></span> | <span data-ttu-id="50b72-119">string</span><span class="sxs-lookup"><span data-stu-id="50b72-119">string</span></span> | <span data-ttu-id="50b72-120">Nom de langage qui identifie la culture des chaînes localisées dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="50b72-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="50b72-121">Par exemple, « en-US » pour l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="50b72-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50b72-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b72-122">Requirements</span></span>



| <span data-ttu-id="50b72-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50b72-123">Requirement</span></span> | <span data-ttu-id="50b72-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b72-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50b72-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b72-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50b72-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50b72-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50b72-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b72-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50b72-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50b72-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50b72-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b72-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="50b72-130">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="50b72-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="50b72-131">**localisation (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="50b72-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





