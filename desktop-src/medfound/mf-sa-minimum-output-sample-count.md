---
description: Spécifie le nombre maximal d’échantillons de sortie qu’une Microsoft Media Foundation transformation (MFT) aura en suspens dans le pipeline à tout moment.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Attribut MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201722"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="86c93-103">\_Attribut de \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="86c93-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="86c93-104">Spécifie le nombre maximal d’échantillons de sortie qu’une Microsoft Media Foundation transformation (MFT) aura en suspens dans le pipeline à tout moment.</span><span class="sxs-lookup"><span data-stu-id="86c93-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="86c93-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="86c93-105">Data type</span></span>

<span data-ttu-id="86c93-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="86c93-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="86c93-107">Notes</span><span class="sxs-lookup"><span data-stu-id="86c93-107">Remarks</span></span>

<span data-ttu-id="86c93-108">Cet attribut s’applique uniquement à MFTs qui utilisent une mémoire tampon circulaire pour allouer leurs propres exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="86c93-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="86c93-109">Les autres MFTs ignorent cet attribut.</span><span class="sxs-lookup"><span data-stu-id="86c93-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="86c93-110">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="86c93-110">To set this attribute:</span></span>

1.  <span data-ttu-id="86c93-111">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="86c93-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="86c93-112">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.</span><span class="sxs-lookup"><span data-stu-id="86c93-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c93-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c93-113">Requirements</span></span>



| <span data-ttu-id="86c93-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86c93-114">Requirement</span></span> | <span data-ttu-id="86c93-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86c93-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c93-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86c93-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86c93-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86c93-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="86c93-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86c93-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86c93-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="86c93-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="86c93-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="86c93-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c93-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c93-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c93-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c93-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c93-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86c93-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86c93-124">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="86c93-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




