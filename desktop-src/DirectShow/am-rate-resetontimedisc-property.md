---
description: S’applique à Windows Vista et versions ultérieures.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545940"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="b4aec-103">\_ \_ Propriété RESETONTIMEDISC rate AM</span><span class="sxs-lookup"><span data-stu-id="b4aec-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="b4aec-104">S’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b4aec-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="b4aec-105">Cette propriété interroge si le décodeur resynchronise les horodatages de sortie aux horodatages d’entrée lorsque le décodeur reçoit un exemple avec l’indicateur de discontinuité.</span><span class="sxs-lookup"><span data-stu-id="b4aec-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="b4aec-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b4aec-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="b4aec-107">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="b4aec-107">Property Set GUID</span></span> | <span data-ttu-id="b4aec-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="b4aec-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="b4aec-109">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="b4aec-109">Property ID</span></span>       | <span data-ttu-id="b4aec-110">\_Taux am \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="b4aec-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="b4aec-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b4aec-111">Data Type</span></span>         | <span data-ttu-id="b4aec-112">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="b4aec-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="b4aec-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b4aec-113">Remarks</span></span>

<span data-ttu-id="b4aec-114">Cette propriété prend en charge les changements de taux d’accélération.</span><span class="sxs-lookup"><span data-stu-id="b4aec-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="b4aec-115">Si la valeur de cette propriété est **true** et que le décodeur reçoit un exemple d’entrée avec l' \_ indicateur AM Sample \_ TIMEDISCONTINUITY, la trame décodée doit avoir le même horodatage que le frame d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b4aec-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="b4aec-116">Pour récupérer l' \_ \_ indicateur TIMEDISCONTINUITY AM, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b4aec-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="b4aec-117">L’indicateur est défini dans le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="b4aec-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="b4aec-118">Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="b4aec-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4aec-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4aec-119">Requirements</span></span>



| <span data-ttu-id="b4aec-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4aec-120">Requirement</span></span> | <span data-ttu-id="b4aec-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4aec-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4aec-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4aec-122">Header</span></span><br/> | <dl> <span data-ttu-id="b4aec-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4aec-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4aec-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4aec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4aec-125">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="b4aec-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




