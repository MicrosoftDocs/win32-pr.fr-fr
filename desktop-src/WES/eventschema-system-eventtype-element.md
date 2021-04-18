---
title: Élément System (EventType)
description: Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- EventLog, élément du système
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512356"
---
# <a name="system-eventtype-element"></a><span data-ttu-id="9dcff-104">Élément System (EventType)</span><span class="sxs-lookup"><span data-stu-id="9dcff-104">System (EventType) Element</span></span>

<span data-ttu-id="9dcff-105">Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.</span><span class="sxs-lookup"><span data-stu-id="9dcff-105">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

<span data-ttu-id="9dcff-106">L’élément **système** est défini par le type complexe [**eventType**](eventschema-eventtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9dcff-106">The **System** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dcff-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dcff-107">Requirements</span></span>



| <span data-ttu-id="9dcff-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dcff-108">Requirement</span></span> | <span data-ttu-id="9dcff-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dcff-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dcff-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dcff-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9dcff-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dcff-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9dcff-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dcff-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9dcff-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dcff-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dcff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dcff-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="9dcff-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="9dcff-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9dcff-116">**événement**</span><span class="sxs-lookup"><span data-stu-id="9dcff-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





