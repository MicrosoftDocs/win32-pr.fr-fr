---
description: Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: Attribut MF_EVENT_START_PRESENTATION_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042859"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="ad0d6-103">\_Attribut heure de la \_ Présentation démarrer l’événement MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad0d6-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="ad0d6-104">Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad0d6-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad0d6-105">Data type</span></span>

<span data-ttu-id="ad0d6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ad0d6-106">**UINT64**</span></span>

<span data-ttu-id="ad0d6-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="ad0d6-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad0d6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ad0d6-108">Remarks</span></span>

<span data-ttu-id="ad0d6-109">Cet attribut est utilisé avec l’événement [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="ad0d6-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="ad0d6-110">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="ad0d6-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad0d6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad0d6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad0d6-112">Requirements</span></span>



| <span data-ttu-id="ad0d6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad0d6-113">Requirement</span></span> | <span data-ttu-id="ad0d6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad0d6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0d6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0d6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ad0d6-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad0d6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad0d6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0d6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ad0d6-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad0d6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad0d6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad0d6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad0d6-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad0d6-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0d6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad0d6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0d6-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad0d6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad0d6-123">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="ad0d6-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad0d6-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ad0d6-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ad0d6-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ad0d6-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




