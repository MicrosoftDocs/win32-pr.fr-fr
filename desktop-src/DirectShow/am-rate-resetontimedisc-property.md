---
description: AM_RATE_ResetOnTimeDisc propriété-s’applique à Windows Vista et versions ultérieures.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096607"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="7ab7d-103">\_ \_ Propriété RESETONTIMEDISC rate AM</span><span class="sxs-lookup"><span data-stu-id="7ab7d-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="7ab7d-104">S’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="7ab7d-105">Cette propriété interroge si le décodeur resynchronise les horodatages de sortie aux horodatages d’entrée lorsque le décodeur reçoit un exemple avec l’indicateur de discontinuité.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="7ab7d-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-106">This property is read/write.</span></span>



| <span data-ttu-id="7ab7d-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="7ab7d-107">Label</span></span> | <span data-ttu-id="7ab7d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ab7d-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="7ab7d-109">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="7ab7d-109">Property Set GUID</span></span> | <span data-ttu-id="7ab7d-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="7ab7d-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="7ab7d-111">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="7ab7d-111">Property ID</span></span>       | <span data-ttu-id="7ab7d-112">\_Taux am \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="7ab7d-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="7ab7d-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ab7d-113">Data Type</span></span>         | <span data-ttu-id="7ab7d-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7ab7d-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="7ab7d-115">Notes </span><span class="sxs-lookup"><span data-stu-id="7ab7d-115">Remarks</span></span>

<span data-ttu-id="7ab7d-116">Cette propriété prend en charge les changements de taux d’accélération.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="7ab7d-117">Si la valeur de cette propriété est **true** et que le décodeur reçoit un exemple d’entrée avec l' \_ indicateur AM Sample \_ TIMEDISCONTINUITY, la trame décodée doit avoir le même horodatage que le frame d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="7ab7d-118">Pour récupérer l' \_ \_ indicateur TIMEDISCONTINUITY AM, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7ab7d-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="7ab7d-119">L’indicateur est défini dans le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="7ab7d-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="7ab7d-120">Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="7ab7d-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab7d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ab7d-121">Requirements</span></span>



| <span data-ttu-id="7ab7d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ab7d-122">Requirement</span></span> | <span data-ttu-id="7ab7d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ab7d-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab7d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ab7d-124">Header</span></span><br/> | <dl> <span data-ttu-id="7ab7d-125"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab7d-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab7d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ab7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab7d-127">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="7ab7d-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




