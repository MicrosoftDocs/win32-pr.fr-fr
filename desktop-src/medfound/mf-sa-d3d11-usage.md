---
description: Spécifie comment allouer des surfaces Microsoft Direct3D 11 pour des exemples de supports.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Attribut MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201723"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="70df2-103">\_Attribut d' \_ utilisation d3d11 MF sa \_</span><span class="sxs-lookup"><span data-stu-id="70df2-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="70df2-104">Spécifie comment allouer des surfaces Microsoft Direct3D 11 pour des exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="70df2-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="70df2-105">L’utilisation de indique directement si un échantillon est accessible par le processeur ou le GPU.</span><span class="sxs-lookup"><span data-stu-id="70df2-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="70df2-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="70df2-106">Data type</span></span>

<span data-ttu-id="70df2-107">**D3d11 \_ UTILISATION** stockée en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70df2-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="70df2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="70df2-108">Remarks</span></span>

<span data-ttu-id="70df2-109">La valeur de cet attribut est une valeur d' [**\_ utilisation d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .</span><span class="sxs-lookup"><span data-stu-id="70df2-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="70df2-110">Transformations de Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70df2-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="70df2-111">Dans ce contexte, l’attribut s’applique uniquement lorsque la Microsoft Media Foundation transformation (MFT) renvoie la **valeur true** pour l’attribut [prenant en \_ \_ \_ charge d3d11 MF](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="70df2-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="70df2-112">Si une table MFT prend en charge Direct3D 11, cet attribut fournit un indicateur à la MFT lors de l’allocation des surfaces Microsoft Direct3D pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="70df2-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="70df2-113">Définissez l’attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="70df2-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="70df2-114">Appelez [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) pour accéder au magasin d’attributs MFT.</span><span class="sxs-lookup"><span data-stu-id="70df2-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="70df2-115">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="70df2-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="70df2-116">Le pipeline Media Foundation définit l’attribut avant le démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="70df2-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="70df2-117">La table MFT doit tenter d’honorer le paramètre lorsqu’il alloue des surfaces.</span><span class="sxs-lookup"><span data-stu-id="70df2-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="70df2-118">Si ce n’est pas possible, la table MFT peut ignorer l’attribut, au lieu d’échouer à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="70df2-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="70df2-119">En outre, si la table MFT requiert des surfaces Direct3D pour l’entrée, elle peut exposer cet attribut comme un indicateur pour la façon dont les surfaces d’entrée doivent être allouées.</span><span class="sxs-lookup"><span data-stu-id="70df2-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="70df2-120">Interrogez l’attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="70df2-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="70df2-121">Appelez [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) pour accéder aux attributs du flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="70df2-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="70df2-122">Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="70df2-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="70df2-123">Allocateur d’échantillon</span><span class="sxs-lookup"><span data-stu-id="70df2-123">Sample Allocator</span></span>

<span data-ttu-id="70df2-124">Cet attribut peut être défini sur l’allocateur d’échantillon vidéo, dans la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="70df2-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70df2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70df2-125">Requirements</span></span>



| <span data-ttu-id="70df2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70df2-126">Requirement</span></span> | <span data-ttu-id="70df2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="70df2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70df2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70df2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="70df2-129">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="70df2-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="70df2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70df2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="70df2-131">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="70df2-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="70df2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="70df2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="70df2-133"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="70df2-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70df2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70df2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70df2-135">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70df2-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
