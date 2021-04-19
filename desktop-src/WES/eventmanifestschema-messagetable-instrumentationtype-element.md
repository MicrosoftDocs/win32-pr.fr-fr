---
title: Élément messageTable (EventsType)
description: Contient une référence à une chaîne dans la section localisation du manifeste. | Élément messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- EventLog, élément messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537203"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="a4cb0-105">Élément messageTable (EventsType)</span><span class="sxs-lookup"><span data-stu-id="a4cb0-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="a4cb0-106">Contient une référence à une chaîne dans la section localisation du manifeste.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a4cb0-107">L’élément **messageTable** est défini par le type complexe [**EventsType**](eventmanifestschema-eventstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a4cb0-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a4cb0-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a4cb0-108">Child elements</span></span>



| <span data-ttu-id="a4cb0-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a4cb0-109">Element</span></span>                                                             | <span data-ttu-id="a4cb0-110">Type</span><span class="sxs-lookup"><span data-stu-id="a4cb0-110">Type</span></span> | <span data-ttu-id="a4cb0-111">Description</span><span class="sxs-lookup"><span data-stu-id="a4cb0-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4cb0-112">**Message**</span><span class="sxs-lookup"><span data-stu-id="a4cb0-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="a4cb0-113">Spécifie une référence à une chaîne dans la section localisation du manifeste.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a4cb0-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="a4cb0-114">Attributes</span></span>



| <span data-ttu-id="a4cb0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="a4cb0-115">Name</span></span>    | <span data-ttu-id="a4cb0-116">Type</span><span class="sxs-lookup"><span data-stu-id="a4cb0-116">Type</span></span>   | <span data-ttu-id="a4cb0-117">Description</span><span class="sxs-lookup"><span data-stu-id="a4cb0-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4cb0-118">message</span><span class="sxs-lookup"><span data-stu-id="a4cb0-118">message</span></span> | <span data-ttu-id="a4cb0-119">string</span><span class="sxs-lookup"><span data-stu-id="a4cb0-119">string</span></span> | <span data-ttu-id="a4cb0-120">Référence à la chaîne localisée dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="a4cb0-121">mid</span><span class="sxs-lookup"><span data-stu-id="a4cb0-121">mid</span></span>     | <span data-ttu-id="a4cb0-122">string</span><span class="sxs-lookup"><span data-stu-id="a4cb0-122">string</span></span> | <span data-ttu-id="a4cb0-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="a4cb0-124">symbole</span><span class="sxs-lookup"><span data-stu-id="a4cb0-124">symbol</span></span>  | <span data-ttu-id="a4cb0-125">string</span><span class="sxs-lookup"><span data-stu-id="a4cb0-125">string</span></span> | <span data-ttu-id="a4cb0-126">Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="a4cb0-127">value</span><span class="sxs-lookup"><span data-stu-id="a4cb0-127">value</span></span>   | <span data-ttu-id="a4cb0-128">string</span><span class="sxs-lookup"><span data-stu-id="a4cb0-128">string</span></span> | <span data-ttu-id="a4cb0-129">Nombre à utiliser comme identificateur de message pour ce message.</span><span class="sxs-lookup"><span data-stu-id="a4cb0-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="a4cb0-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4cb0-130">Requirements</span></span>



| <span data-ttu-id="a4cb0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4cb0-131">Requirement</span></span> | <span data-ttu-id="a4cb0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4cb0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4cb0-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4cb0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a4cb0-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4cb0-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4cb0-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4cb0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a4cb0-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4cb0-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4cb0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4cb0-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4cb0-138">**Éléments parents**</span><span class="sxs-lookup"><span data-stu-id="a4cb0-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="a4cb0-139">**Élément Events (InstrumentationType)**</span><span class="sxs-lookup"><span data-stu-id="a4cb0-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





