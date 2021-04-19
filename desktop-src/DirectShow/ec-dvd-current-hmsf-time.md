---
description: Signale l’heure actuelle, au \_ \_ format de code temporel DVD HMSF par rapport au début du titre. Cet événement est déclenché au début de chaque VOBU, qui se produit toutes les 0,4 à 1,0 secondes.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528637"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="261d5-104">\_ \_ \_ temps HMSF actuel du \_ DVD</span><span class="sxs-lookup"><span data-stu-id="261d5-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="261d5-105">Signale l’heure actuelle, au format de [**\_ \_ code temporel DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) par rapport au début du titre.</span><span class="sxs-lookup"><span data-stu-id="261d5-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="261d5-106">Cet événement est déclenché au début de chaque VOBU, qui se produit toutes les 0,4 à 1,0 secondes.</span><span class="sxs-lookup"><span data-stu-id="261d5-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="261d5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="261d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261d5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="261d5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="261d5-109">Valeur ULONG qui contient la structure du \_ \_ code temporel DVD HMSF.</span><span class="sxs-lookup"><span data-stu-id="261d5-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="261d5-110">Affectez lParam1 à une variable ULONG, puis effectuez un cast de cette variable en un \_ \_ code temporel DVD HMSF pour accéder à ses valeurs.</span><span class="sxs-lookup"><span data-stu-id="261d5-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="261d5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="261d5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="261d5-112">Valeur ULONG contenant une Union d' [**indicateurs de \_ code \_ temporel DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span><span class="sxs-lookup"><span data-stu-id="261d5-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="261d5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="261d5-113">Remarks</span></span>

<span data-ttu-id="261d5-114">Le \_ format de \_ code temporel DVD HMSF est destiné à remplacer l’ancien format BCD renvoyé dans les \_ \_ événements de temps courant du DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="261d5-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="261d5-115">Les codes temporels HMSF sont plus faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="261d5-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="261d5-116">Pour que le navigateur envoie les \_ \_ \_ \_ événements HMSF de temps du DVD en cours au lieu des \_ \_ événements temps courant du DVD \_ , une application doit appeler `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="261d5-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="261d5-117">Lorsque cet indicateur est défini, le navigateur s’attend également à ce que tous les paramètres de temps dans les méthodes [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) soient passés comme des \_ \_ codes temporels de DVD HMSF.</span><span class="sxs-lookup"><span data-stu-id="261d5-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="261d5-118">Cet événement est déclenché dans les domaines de titre.</span><span class="sxs-lookup"><span data-stu-id="261d5-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="261d5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="261d5-119">Requirements</span></span>



| <span data-ttu-id="261d5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="261d5-120">Requirement</span></span> | <span data-ttu-id="261d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="261d5-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="261d5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="261d5-122">Header</span></span><br/> | <dl> <span data-ttu-id="261d5-123"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="261d5-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261d5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="261d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261d5-125">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="261d5-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="261d5-126">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="261d5-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="261d5-127">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="261d5-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




