---
description: Spécifie l’état d’une topologie pendant la lecture.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: Attribut MF_EVENT_TOPOLOGY_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532164"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="a5444-103">Attribut d’état de la \_ topologie des événements MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="a5444-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="a5444-104">Spécifie l’état d’une topologie pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="a5444-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5444-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5444-105">Data type</span></span>

<span data-ttu-id="a5444-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5444-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5444-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a5444-107">Remarks</span></span>

<span data-ttu-id="a5444-108">La valeur de cet attribut est un membre de l’énumération [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .</span><span class="sxs-lookup"><span data-stu-id="a5444-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="a5444-109">Cet attribut est utilisé avec l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a5444-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="a5444-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a5444-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5444-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5444-111">Requirements</span></span>



| <span data-ttu-id="a5444-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5444-112">Requirement</span></span> | <span data-ttu-id="a5444-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5444-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5444-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5444-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a5444-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5444-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5444-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5444-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a5444-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5444-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5444-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5444-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5444-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5444-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5444-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5444-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5444-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5444-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5444-122">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="a5444-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5444-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5444-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a5444-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5444-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




