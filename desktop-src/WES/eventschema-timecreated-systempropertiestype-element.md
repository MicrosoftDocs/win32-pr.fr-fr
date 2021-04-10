---
title: Élément TimeCreated (SystemPropertiesType)
description: Horodatage qui identifie le moment où l’événement a été enregistré.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog, élément TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942314"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="4a726-104">Élément TimeCreated (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="4a726-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="4a726-105">Horodatage qui identifie le moment où l’événement a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="4a726-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4a726-106">L’élément **TimeCreated** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a726-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="4a726-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4a726-107">Attributes</span></span>



| <span data-ttu-id="4a726-108">Nom</span><span class="sxs-lookup"><span data-stu-id="4a726-108">Name</span></span>       | <span data-ttu-id="4a726-109">Type</span><span class="sxs-lookup"><span data-stu-id="4a726-109">Type</span></span>     | <span data-ttu-id="4a726-110">Description</span><span class="sxs-lookup"><span data-stu-id="4a726-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="4a726-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="4a726-111">SystemTime</span></span> | <span data-ttu-id="4a726-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="4a726-112">dateTime</span></span> | <span data-ttu-id="4a726-113">Heure système de la journalisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="4a726-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4a726-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a726-114">Requirements</span></span>



| <span data-ttu-id="4a726-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a726-115">Requirement</span></span> | <span data-ttu-id="4a726-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a726-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a726-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a726-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a726-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a726-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a726-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a726-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a726-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a726-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a726-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a726-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a726-122">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="4a726-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="4a726-123">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="4a726-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





