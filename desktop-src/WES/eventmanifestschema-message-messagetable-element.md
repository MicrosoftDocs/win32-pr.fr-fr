---
title: Élément message (messageTable)
description: Contient une référence à une chaîne dans la section localisation du manifeste. | Élément message (messageTable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- message, élément EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106536231"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="d2506-105">Élément message (messageTable)</span><span class="sxs-lookup"><span data-stu-id="d2506-105">message (messageTable) Element</span></span>

<span data-ttu-id="d2506-106">Contient une référence à une chaîne dans la section localisation du manifeste.</span><span class="sxs-lookup"><span data-stu-id="d2506-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d2506-107">L’élément **message** est défini par l’élément [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d2506-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="d2506-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="d2506-108">Attributes</span></span>



| <span data-ttu-id="d2506-109">Nom</span><span class="sxs-lookup"><span data-stu-id="d2506-109">Name</span></span>    | <span data-ttu-id="d2506-110">Type</span><span class="sxs-lookup"><span data-stu-id="d2506-110">Type</span></span>   | <span data-ttu-id="d2506-111">Description</span><span class="sxs-lookup"><span data-stu-id="d2506-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2506-112">message</span><span class="sxs-lookup"><span data-stu-id="d2506-112">message</span></span> | <span data-ttu-id="d2506-113">string</span><span class="sxs-lookup"><span data-stu-id="d2506-113">string</span></span> | <span data-ttu-id="d2506-114">Référence à la chaîne localisée dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d2506-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="d2506-115">mid</span><span class="sxs-lookup"><span data-stu-id="d2506-115">mid</span></span>     | <span data-ttu-id="d2506-116">string</span><span class="sxs-lookup"><span data-stu-id="d2506-116">string</span></span> | <span data-ttu-id="d2506-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d2506-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="d2506-118">symbole</span><span class="sxs-lookup"><span data-stu-id="d2506-118">symbol</span></span>  | <span data-ttu-id="d2506-119">string</span><span class="sxs-lookup"><span data-stu-id="d2506-119">string</span></span> | <span data-ttu-id="d2506-120">Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="d2506-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="d2506-121">value</span><span class="sxs-lookup"><span data-stu-id="d2506-121">value</span></span>   | <span data-ttu-id="d2506-122">string</span><span class="sxs-lookup"><span data-stu-id="d2506-122">string</span></span> | <span data-ttu-id="d2506-123">Nombre à utiliser comme identificateur de message pour ce message.</span><span class="sxs-lookup"><span data-stu-id="d2506-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="d2506-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2506-124">Requirements</span></span>



| <span data-ttu-id="d2506-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2506-125">Requirement</span></span> | <span data-ttu-id="d2506-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2506-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2506-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2506-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d2506-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2506-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2506-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2506-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d2506-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2506-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2506-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2506-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2506-132">**Éléments parents**</span><span class="sxs-lookup"><span data-stu-id="d2506-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="d2506-133">**messageTable (EventsType)**</span><span class="sxs-lookup"><span data-stu-id="d2506-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="d2506-134">**messageTable (type de données)**</span><span class="sxs-lookup"><span data-stu-id="d2506-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





