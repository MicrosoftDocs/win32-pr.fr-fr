---
description: Spécifie si la source de Sequencer a annulé une topologie.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Attribut MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522838"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="f9018-103">Attribut d’annulation de la topologie de la \_ source d’événements MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f9018-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="f9018-104">Spécifie si la [source de Sequencer](sequencer-source.md) a annulé une topologie.</span><span class="sxs-lookup"><span data-stu-id="f9018-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9018-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9018-105">Data type</span></span>

<span data-ttu-id="f9018-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f9018-106">**UINT32**</span></span>

<span data-ttu-id="f9018-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="f9018-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9018-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f9018-108">Remarks</span></span>

<span data-ttu-id="f9018-109">Cet attribut est utilisé avec les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="f9018-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="f9018-110">MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="f9018-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="f9018-111">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="f9018-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="f9018-112">Si cet attribut est présent et différent de zéro, cela signifie que le segment de présentation s’est terminé parce que la source de Sequencer a annulé la topologie.</span><span class="sxs-lookup"><span data-stu-id="f9018-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="f9018-113">Dans le cas contraire, le segment de présentation s’est terminé normalement.</span><span class="sxs-lookup"><span data-stu-id="f9018-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="f9018-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f9018-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9018-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9018-115">Requirements</span></span>



| <span data-ttu-id="f9018-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9018-116">Requirement</span></span> | <span data-ttu-id="f9018-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9018-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9018-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9018-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9018-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9018-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9018-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9018-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9018-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9018-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9018-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9018-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9018-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9018-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9018-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9018-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9018-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9018-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9018-126">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="f9018-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f9018-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f9018-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f9018-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f9018-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f9018-129">Événements de source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="f9018-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




