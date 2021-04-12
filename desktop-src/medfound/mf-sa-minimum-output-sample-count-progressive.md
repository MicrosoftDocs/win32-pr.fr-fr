---
description: Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Attribut MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203715"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="dd5f5-103">\_ \_ \_ \_ \_ \_ Attribut progressif du nombre minimal d’échantillons de sortie MF sa</span><span class="sxs-lookup"><span data-stu-id="dd5f5-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="dd5f5-104">Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="dd5f5-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="dd5f5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dd5f5-105">Data type</span></span>

<span data-ttu-id="dd5f5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dd5f5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dd5f5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dd5f5-107">Remarks</span></span>

<span data-ttu-id="dd5f5-108">Cet attribut s’applique uniquement à MFTs qui utilisent une mémoire tampon circulaire pour allouer leurs propres exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="dd5f5-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="dd5f5-109">Les autres MFTs ignorent cet attribut.</span><span class="sxs-lookup"><span data-stu-id="dd5f5-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="dd5f5-110">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="dd5f5-110">To set this attribute:</span></span>

1.  <span data-ttu-id="dd5f5-111">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="dd5f5-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="dd5f5-112">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.</span><span class="sxs-lookup"><span data-stu-id="dd5f5-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5f5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd5f5-113">Requirements</span></span>



| <span data-ttu-id="dd5f5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd5f5-114">Requirement</span></span> | <span data-ttu-id="dd5f5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd5f5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5f5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd5f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5f5-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd5f5-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="dd5f5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd5f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5f5-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="dd5f5-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dd5f5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd5f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd5f5-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd5f5-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5f5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd5f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5f5-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd5f5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




