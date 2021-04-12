---
title: Élément Binary (EventDataType)
description: Objet blob de données binaires pour les événements écrits à l’aide de la journalisation des événements.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Élément binaire EventLog
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032370"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="75c5a-104">Élément Binary (EventDataType)</span><span class="sxs-lookup"><span data-stu-id="75c5a-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="75c5a-105">Objet blob de données binaires pour les événements écrits à l’aide de la [journalisation des événements](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="75c5a-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="75c5a-106">L’élément **binaire** est défini par le type complexe [**EventDataType**](eventschema-eventdatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75c5a-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c5a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75c5a-107">Requirements</span></span>



| <span data-ttu-id="75c5a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75c5a-108">Requirement</span></span> | <span data-ttu-id="75c5a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="75c5a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75c5a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c5a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="75c5a-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75c5a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75c5a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75c5a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="75c5a-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75c5a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75c5a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75c5a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="75c5a-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="75c5a-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="75c5a-116">**EventData (EventType)**</span><span class="sxs-lookup"><span data-stu-id="75c5a-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

