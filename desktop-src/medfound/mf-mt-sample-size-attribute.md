---
description: Spécifie la taille de chaque échantillon, en octets, dans un type de média.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: Attribut MF_MT_SAMPLE_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530846"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="ad4c2-103">\_Attribut de \_ taille d’exemple MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad4c2-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="ad4c2-104">Spécifie la taille de chaque échantillon, en octets, dans un type de média.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad4c2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad4c2-105">Data type</span></span>

<span data-ttu-id="ad4c2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad4c2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad4c2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ad4c2-107">Remarks</span></span>

<span data-ttu-id="ad4c2-108">Cet attribut est valide uniquement si l’attribut d' [**\_ \_ \_ \_ échantillons de taille fixe MF MT**](mf-mt-fixed-size-samples-attribute.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="ad4c2-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad4c2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad4c2-110">Requirements</span></span>



| <span data-ttu-id="ad4c2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad4c2-111">Requirement</span></span> | <span data-ttu-id="ad4c2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad4c2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4c2-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad4c2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ad4c2-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad4c2-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ad4c2-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad4c2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ad4c2-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad4c2-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ad4c2-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad4c2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad4c2-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad4c2-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4c2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad4c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4c2-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad4c2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad4c2-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ad4c2-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ad4c2-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ad4c2-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ad4c2-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ad4c2-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ad4c2-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="ad4c2-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




