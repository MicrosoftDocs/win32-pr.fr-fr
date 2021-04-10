---
title: Élément String (StringTableType)
description: Définit une chaîne localisée.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- élément String EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942315"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="24b9b-104">Élément String (StringTableType)</span><span class="sxs-lookup"><span data-stu-id="24b9b-104">string (StringTableType) Element</span></span>

<span data-ttu-id="24b9b-105">Définit une chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="24b9b-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

<span data-ttu-id="24b9b-106">L’élément **String** est défini par le type complexe [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="24b9b-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="24b9b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="24b9b-107">Attributes</span></span>



| <span data-ttu-id="24b9b-108">Nom</span><span class="sxs-lookup"><span data-stu-id="24b9b-108">Name</span></span>       | <span data-ttu-id="24b9b-109">Type</span><span class="sxs-lookup"><span data-stu-id="24b9b-109">Type</span></span>   | <span data-ttu-id="24b9b-110">Description</span><span class="sxs-lookup"><span data-stu-id="24b9b-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24b9b-111">id</span><span class="sxs-lookup"><span data-stu-id="24b9b-111">id</span></span>         | <span data-ttu-id="24b9b-112">string</span><span class="sxs-lookup"><span data-stu-id="24b9b-112">string</span></span> | <span data-ttu-id="24b9b-113">Identificateur qui identifie de façon unique la chaîne dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="24b9b-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="24b9b-114">stringType</span><span class="sxs-lookup"><span data-stu-id="24b9b-114">stringType</span></span> | <span data-ttu-id="24b9b-115">string</span><span class="sxs-lookup"><span data-stu-id="24b9b-115">string</span></span> | <span data-ttu-id="24b9b-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24b9b-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="24b9b-117">value</span><span class="sxs-lookup"><span data-stu-id="24b9b-117">value</span></span>      | <span data-ttu-id="24b9b-118">string</span><span class="sxs-lookup"><span data-stu-id="24b9b-118">string</span></span> | <span data-ttu-id="24b9b-119">La chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="24b9b-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="24b9b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24b9b-120">Requirements</span></span>



| <span data-ttu-id="24b9b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24b9b-121">Requirement</span></span> | <span data-ttu-id="24b9b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="24b9b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24b9b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="24b9b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24b9b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24b9b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="24b9b-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24b9b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24b9b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24b9b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="24b9b-128">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="24b9b-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="24b9b-129">**stringTable (LocalizationType)**</span><span class="sxs-lookup"><span data-stu-id="24b9b-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





