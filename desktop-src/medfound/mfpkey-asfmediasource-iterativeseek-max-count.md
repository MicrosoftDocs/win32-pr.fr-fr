---
description: Définit le nombre maximal d’itérations de recherche que la source de média ASF utilisera lors de la recherche itérative.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523754"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="6d9a9-103">\_Propriété MFPKEY ASFMediaSource \_ IterativeSeek \_ Max \_ Count</span><span class="sxs-lookup"><span data-stu-id="6d9a9-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="6d9a9-104">Définit le nombre maximal d’itérations de recherche que la source de média ASF utilisera lors de la recherche itérative.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="6d9a9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6d9a9-105">Data type</span></span>

<span data-ttu-id="6d9a9-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6d9a9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6d9a9-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6d9a9-107">PROPVARIANT member</span></span>

<span data-ttu-id="6d9a9-108">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="6d9a9-108">**ULONG**</span></span>

<span data-ttu-id="6d9a9-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6d9a9-109">VT\_UI4</span></span>

<span data-ttu-id="6d9a9-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="6d9a9-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6d9a9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6d9a9-111">Remarks</span></span>

<span data-ttu-id="6d9a9-112">Utilisez cette propriété pour configurer la source de média ASF.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="6d9a9-113">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="6d9a9-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6d9a9-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="6d9a9-115">Cette propriété s’applique uniquement lorsque la recherche itérative est activée.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="6d9a9-116">Pour plus d’informations, consultez [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="6d9a9-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="6d9a9-117">La plage valide de cette propriété est \[ 1-10 \] , inclus.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="6d9a9-118">Avec un nombre plus élevé, la recherche itérative a tendance à être plus précise, mais elle prend plus de temps.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="6d9a9-119">La valeur par défaut est 5.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9a9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d9a9-120">Requirements</span></span>



| <span data-ttu-id="6d9a9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d9a9-121">Requirement</span></span> | <span data-ttu-id="6d9a9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d9a9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9a9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9a9-124">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6d9a9-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6d9a9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9a9-126">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6d9a9-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6d9a9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d9a9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d9a9-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9a9-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9a9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d9a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9a9-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d9a9-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




