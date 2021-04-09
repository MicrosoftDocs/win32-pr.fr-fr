---
description: Décalage entre l’heure de présentation et les horodatages de la source du média.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Attribut MF_EVENT_PRESENTATION_TIME_OFFSET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862958"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="821ef-103">Attribut de décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="821ef-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="821ef-104">Décalage entre l’heure de présentation et les horodatages de la source du média.</span><span class="sxs-lookup"><span data-stu-id="821ef-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="821ef-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="821ef-105">Data type</span></span>

<span data-ttu-id="821ef-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="821ef-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="821ef-107">Notes</span><span class="sxs-lookup"><span data-stu-id="821ef-107">Remarks</span></span>

<span data-ttu-id="821ef-108">Le décalage est calculé comme suit : décalage = heure de la présentation − heure source.</span><span class="sxs-lookup"><span data-stu-id="821ef-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="821ef-109">Cet attribut est utilisé avec les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="821ef-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="821ef-110">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="821ef-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="821ef-111">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="821ef-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="821ef-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="821ef-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="821ef-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="821ef-113">Requirements</span></span>



| <span data-ttu-id="821ef-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="821ef-114">Requirement</span></span> | <span data-ttu-id="821ef-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="821ef-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="821ef-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="821ef-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="821ef-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="821ef-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="821ef-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="821ef-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="821ef-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="821ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="821ef-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="821ef-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="821ef-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="821ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821ef-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="821ef-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="821ef-124">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="821ef-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="821ef-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="821ef-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="821ef-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="821ef-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




