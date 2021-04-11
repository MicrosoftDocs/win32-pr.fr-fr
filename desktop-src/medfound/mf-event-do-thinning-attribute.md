---
description: Quand une source de média demande un nouveau taux de lecture, cet attribut spécifie si la source demande également une éclaircie. Pour obtenir une définition de la réduction, consultez à propos du contrôle du taux.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Attribut MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951296"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="3e57a-104">\_Attribut de \_ fin d’événement MF \_</span><span class="sxs-lookup"><span data-stu-id="3e57a-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="3e57a-105">Quand une source de média demande un nouveau taux de lecture, cet attribut spécifie si la source demande également une éclaircie.</span><span class="sxs-lookup"><span data-stu-id="3e57a-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="3e57a-106">Pour obtenir une définition de la réduction, consultez [à propos du contrôle du taux](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="3e57a-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="3e57a-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="3e57a-107">Data type</span></span>

<span data-ttu-id="3e57a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e57a-108">**UINT32**</span></span>

<span data-ttu-id="3e57a-109">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="3e57a-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e57a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3e57a-110">Remarks</span></span>

<span data-ttu-id="3e57a-111">Cet attribut est utilisé avec l’événement [MESourceRateChangeRequested](mesourceratechangerequested.md) .</span><span class="sxs-lookup"><span data-stu-id="3e57a-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="3e57a-112">Si la valeur est **true**, la source du média demande un commutateur à une lecture fine.</span><span class="sxs-lookup"><span data-stu-id="3e57a-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="3e57a-113">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3e57a-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="3e57a-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3e57a-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e57a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e57a-115">Requirements</span></span>



| <span data-ttu-id="3e57a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e57a-116">Requirement</span></span> | <span data-ttu-id="3e57a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e57a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e57a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e57a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3e57a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e57a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e57a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e57a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3e57a-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e57a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e57a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e57a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e57a-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e57a-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e57a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e57a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e57a-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e57a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e57a-126">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="3e57a-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e57a-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3e57a-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3e57a-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3e57a-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




