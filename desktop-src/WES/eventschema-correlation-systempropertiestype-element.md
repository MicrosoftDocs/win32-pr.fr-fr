---
title: Élément correlation (SystemPropertiesType)
description: Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Élément de corrélation EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942577"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="7a45b-104">Élément correlation (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="7a45b-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="7a45b-105">Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.</span><span class="sxs-lookup"><span data-stu-id="7a45b-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7a45b-106">L’élément **Correlation** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7a45b-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="7a45b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="7a45b-107">Attributes</span></span>



| <span data-ttu-id="7a45b-108">Nom</span><span class="sxs-lookup"><span data-stu-id="7a45b-108">Name</span></span>              | <span data-ttu-id="7a45b-109">Type</span><span class="sxs-lookup"><span data-stu-id="7a45b-109">Type</span></span>                                                | <span data-ttu-id="7a45b-110">Description</span><span class="sxs-lookup"><span data-stu-id="7a45b-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a45b-111">ActivityID</span><span class="sxs-lookup"><span data-stu-id="7a45b-111">ActivityID</span></span>        | [<span data-ttu-id="7a45b-112">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="7a45b-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="7a45b-113">Identificateur global unique qui identifie l’activité en cours.</span><span class="sxs-lookup"><span data-stu-id="7a45b-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="7a45b-114">Les événements qui sont publiés avec cet identificateur font partie de la même activité.</span><span class="sxs-lookup"><span data-stu-id="7a45b-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="7a45b-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="7a45b-115">RelatedActivityID</span></span> | [<span data-ttu-id="7a45b-116">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="7a45b-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="7a45b-117">Identificateur global unique qui identifie l’activité à laquelle le contrôle a été transféré.</span><span class="sxs-lookup"><span data-stu-id="7a45b-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="7a45b-118">Les événements connexes ont alors cet identificateur comme identificateur ActivityID.</span><span class="sxs-lookup"><span data-stu-id="7a45b-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7a45b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a45b-119">Requirements</span></span>



| <span data-ttu-id="7a45b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a45b-120">Requirement</span></span> | <span data-ttu-id="7a45b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a45b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a45b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a45b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a45b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a45b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a45b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a45b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a45b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a45b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a45b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a45b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a45b-127">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="7a45b-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="7a45b-128">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="7a45b-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





