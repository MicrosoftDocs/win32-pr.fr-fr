---
description: Spécifie pour un type de média si les échantillons ont une taille fixe.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: Attribut MF_MT_FIXED_SIZE_SAMPLES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518159"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="ee8d7-103">\_Attribut d' \_ \_ échantillons de taille fixe \_ pour MF MT</span><span class="sxs-lookup"><span data-stu-id="ee8d7-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="ee8d7-104">Spécifie pour un type de média si les échantillons ont une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="ee8d7-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee8d7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ee8d7-105">Data type</span></span>

<span data-ttu-id="ee8d7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ee8d7-106">**UINT32**</span></span>

<span data-ttu-id="ee8d7-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="ee8d7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee8d7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ee8d7-108">Remarks</span></span>

<span data-ttu-id="ee8d7-109">Si cet attribut a la **valeur true**, chaque échantillon dans le flux a la même taille (en octets).</span><span class="sxs-lookup"><span data-stu-id="ee8d7-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="ee8d7-110">Dans le cas contraire, les échantillons peuvent varier en taille.</span><span class="sxs-lookup"><span data-stu-id="ee8d7-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="ee8d7-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ee8d7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8d7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee8d7-112">Requirements</span></span>



| <span data-ttu-id="ee8d7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee8d7-113">Requirement</span></span> | <span data-ttu-id="ee8d7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee8d7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8d7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee8d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8d7-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="ee8d7-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ee8d7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee8d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8d7-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ee8d7-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ee8d7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee8d7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee8d7-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d7-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8d7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee8d7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8d7-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee8d7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee8d7-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee8d7-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ee8d7-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee8d7-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ee8d7-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ee8d7-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ee8d7-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="ee8d7-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




