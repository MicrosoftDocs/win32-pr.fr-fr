---
description: Spécifie si la source du média ASF utilise la recherche approximative.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524777"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="58a62-103">MFPKEY \_ ASFMediaSource \_ ApproxSeek, propriété</span><span class="sxs-lookup"><span data-stu-id="58a62-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="58a62-104">Spécifie si la source du média ASF utilise la recherche approximative.</span><span class="sxs-lookup"><span data-stu-id="58a62-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="58a62-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="58a62-105">Data type</span></span>

<span data-ttu-id="58a62-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="58a62-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="58a62-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="58a62-107">PROPVARIANT member</span></span>

<span data-ttu-id="58a62-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="58a62-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="58a62-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="58a62-109">VT\_BOOL</span></span>

<span data-ttu-id="58a62-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="58a62-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="58a62-111">Notes</span><span class="sxs-lookup"><span data-stu-id="58a62-111">Remarks</span></span>

<span data-ttu-id="58a62-112">Les applications peuvent utiliser cette propriété pour configurer la source de média ASF.</span><span class="sxs-lookup"><span data-stu-id="58a62-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="58a62-113">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="58a62-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="58a62-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="58a62-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="58a62-115">La source du média ASF gère la recherche comme suit :</span><span class="sxs-lookup"><span data-stu-id="58a62-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="58a62-116">Si la valeur de cette propriété est **\_ true**, la source du média utilise une recherche approximative, ce qui est moins précis mais plus rapide que la recherche exacte.</span><span class="sxs-lookup"><span data-stu-id="58a62-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="58a62-117">Si la valeur est **\_ false** et que le fichier ASF a un index, la source du média utilise la recherche exacte.</span><span class="sxs-lookup"><span data-stu-id="58a62-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="58a62-118">Si le fichier ASF ne contient pas d’index, la source du média utilise la recherche approxmate, sauf si la propriété [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) est définie sur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="58a62-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="58a62-119">Si le fichier ASF ne contient pas d’index et que la propriété [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) a la **\_ valeur variant true**, la source du média utilise la recherche itérative.</span><span class="sxs-lookup"><span data-stu-id="58a62-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="58a62-120">La recherche itérative est plus précise, mais plus lente que la recherche approximative (mais généralement moins précise que la recherche exacte).</span><span class="sxs-lookup"><span data-stu-id="58a62-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="58a62-121">Requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="58a62-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="58a62-122">La valeur par défaut de cette propriété **est \_ false false**.</span><span class="sxs-lookup"><span data-stu-id="58a62-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a62-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58a62-123">Requirements</span></span>



| <span data-ttu-id="58a62-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58a62-124">Requirement</span></span> | <span data-ttu-id="58a62-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="58a62-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58a62-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a62-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58a62-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a62-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="58a62-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58a62-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58a62-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58a62-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58a62-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="58a62-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="58a62-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58a62-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a62-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58a62-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a62-133">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58a62-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




