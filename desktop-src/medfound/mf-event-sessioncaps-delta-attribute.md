---
description: Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Attribut MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393532"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="d1823-103">\_Attribut de \_ Delta SESSIONCAPS d’événement MF \_</span><span class="sxs-lookup"><span data-stu-id="d1823-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="d1823-104">Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="d1823-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1823-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d1823-105">Data type</span></span>

<span data-ttu-id="d1823-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d1823-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1823-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d1823-107">Remarks</span></span>

<span data-ttu-id="d1823-108">Cet attribut contient un masque de masque indiquant les fonctionnalités qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="d1823-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="d1823-109">Pour obtenir la liste des indicateurs possibles, consultez [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="d1823-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="d1823-110">Les bits sont définis sur 1 dans le masque de bits pour l’une des raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1823-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="d1823-111">Le bit des fonctionnalités correspondant est passé de 0 à 1.</span><span class="sxs-lookup"><span data-stu-id="d1823-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="d1823-112">Le bit des fonctionnalités correspondant est passé de 1 à 0.</span><span class="sxs-lookup"><span data-stu-id="d1823-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="d1823-113">Le bit des fonctionnalités correspondant est resté 1, mais les détails de la fonctionnalité ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="d1823-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="d1823-114">Par exemple, le taux de lecture maximal a changé.</span><span class="sxs-lookup"><span data-stu-id="d1823-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="d1823-115">Cet attribut est utilisé avec l’événement [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d1823-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="d1823-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d1823-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1823-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1823-117">Requirements</span></span>



| <span data-ttu-id="d1823-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1823-118">Requirement</span></span> | <span data-ttu-id="d1823-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1823-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1823-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1823-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1823-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1823-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d1823-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1823-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1823-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1823-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1823-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1823-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1823-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1823-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1823-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1823-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1823-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1823-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1823-128">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="d1823-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1823-129">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d1823-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d1823-130">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d1823-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




