---
description: Spécifie l’heure de début d’une topologie de segment.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: Attribut MF_EVENT_SOURCE_PROJECTSTART (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869117"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="1fcd8-103">\_Attribut PROJECTSTART de la source d’événement MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="1fcd8-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="1fcd8-104">Spécifie l’heure de début d’une topologie de segment.</span><span class="sxs-lookup"><span data-stu-id="1fcd8-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="1fcd8-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1fcd8-105">Data type</span></span>

<span data-ttu-id="1fcd8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1fcd8-106">**UINT64**</span></span>

<span data-ttu-id="1fcd8-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="1fcd8-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcd8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1fcd8-108">Remarks</span></span>

<span data-ttu-id="1fcd8-109">Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcd8-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="1fcd8-110">La source de Sequencer définit cet attribut lorsque la topologie de segment actuelle a l' [**attribut \_ \_ PROJECTSTART de topologie MF**](mf-topology-projectstart-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcd8-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="1fcd8-111">Les deux attributs ont la même valeur.</span><span class="sxs-lookup"><span data-stu-id="1fcd8-111">The two attributes have the same value.</span></span>

<span data-ttu-id="1fcd8-112">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="1fcd8-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="1fcd8-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1fcd8-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcd8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fcd8-114">Requirements</span></span>



| <span data-ttu-id="1fcd8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fcd8-115">Requirement</span></span> | <span data-ttu-id="1fcd8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fcd8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcd8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fcd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcd8-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fcd8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1fcd8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fcd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcd8-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fcd8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1fcd8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fcd8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fcd8-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcd8-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcd8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fcd8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcd8-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1fcd8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1fcd8-125">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="1fcd8-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1fcd8-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1fcd8-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="1fcd8-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1fcd8-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




