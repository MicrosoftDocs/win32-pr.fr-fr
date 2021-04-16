---
title: Élément de latence (ChannelPublishingType)
description: Délai d’attente avant le vidage des mémoires tampons, en millisecondes.
ms.assetid: 7ca6a0f8-3d4c-41e8-a998-0e34d2df4a2f
keywords:
- Journal des événements d’élément de latence
topic_type:
- apiref
api_name:
- latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d48a98f2f319ec08d2fc1325728f798c5ec96e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508285"
---
# <a name="latency-channelpublishingtype-element"></a><span data-ttu-id="a59a2-104">Élément de latence (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="a59a2-104">latency (ChannelPublishingType) Element</span></span>

<span data-ttu-id="a59a2-105">Délai d’attente avant le vidage des mémoires tampons, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a59a2-105">The time to wait before flushing the buffers, in milliseconds.</span></span>

``` syntax
<xs:element name="latency"
    type="unsignedInt"
 />
```

<span data-ttu-id="a59a2-106">L’élément de **latence** est défini par le type complexe [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a59a2-106">The **latency** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a59a2-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a59a2-107">Requirements</span></span>



| <span data-ttu-id="a59a2-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a59a2-108">Requirement</span></span> | <span data-ttu-id="a59a2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a59a2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a59a2-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a59a2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a59a2-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a59a2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a59a2-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a59a2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a59a2-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a59a2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a59a2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a59a2-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a59a2-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="a59a2-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a59a2-116">**publication (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="a59a2-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





