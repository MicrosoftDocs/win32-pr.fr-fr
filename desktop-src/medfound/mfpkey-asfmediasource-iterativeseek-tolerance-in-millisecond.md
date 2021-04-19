---
description: Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523752"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="2353d-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ en \_ millisecondes</span><span class="sxs-lookup"><span data-stu-id="2353d-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="2353d-104">Définit la tolérance, en millisecondes, utilisée lorsque la source de média ASF effectue une recherche itérative.</span><span class="sxs-lookup"><span data-stu-id="2353d-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="2353d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2353d-105">Data type</span></span>

<span data-ttu-id="2353d-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2353d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2353d-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2353d-107">PROPVARIANT member</span></span>

<span data-ttu-id="2353d-108">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="2353d-108">**ULONG**</span></span>

<span data-ttu-id="2353d-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2353d-109">VT\_UI4</span></span>

<span data-ttu-id="2353d-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="2353d-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2353d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2353d-111">Remarks</span></span>

<span data-ttu-id="2353d-112">Utilisez cette propriété pour configurer la source de média ASF.</span><span class="sxs-lookup"><span data-stu-id="2353d-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="2353d-113">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="2353d-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="2353d-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2353d-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="2353d-115">Cette propriété s’applique uniquement lorsque la recherche itérative est activée.</span><span class="sxs-lookup"><span data-stu-id="2353d-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="2353d-116">Pour plus d’informations, consultez [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="2353d-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="2353d-117">L’algorithme de recherche itérative s’arrête s’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2353d-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="2353d-118">La valeur par défaut est 8000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2353d-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="2353d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2353d-119">Requirements</span></span>



| <span data-ttu-id="2353d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2353d-120">Requirement</span></span> | <span data-ttu-id="2353d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2353d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2353d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2353d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2353d-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2353d-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2353d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2353d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2353d-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2353d-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2353d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2353d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2353d-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2353d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2353d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2353d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2353d-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2353d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




