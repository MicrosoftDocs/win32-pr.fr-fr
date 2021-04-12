---
description: Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Attribut MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319310"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="ecabc-103">\_ \_ Attribut BINDFLAGS d3d11 MF sa \_</span><span class="sxs-lookup"><span data-stu-id="ecabc-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="ecabc-104">Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="ecabc-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="ecabc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ecabc-105">Data type</span></span>

<span data-ttu-id="ecabc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ecabc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ecabc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ecabc-107">Remarks</span></span>

<span data-ttu-id="ecabc-108">La **valeur de cet** attribut est une opération or au niveau du bit des indicateurs d' [**\_ \_ indicateur de liaison d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="ecabc-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="ecabc-109">Transformations de Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecabc-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="ecabc-110">Dans ce contexte, l’attribut s’applique uniquement lorsque la Microsoft Media Foundation transformation (MFT) renvoie la **valeur true** pour l’attribut [prenant en \_ \_ \_ charge d3d11 MF](mf-sa-d3d11-aware.md) .</span><span class="sxs-lookup"><span data-stu-id="ecabc-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="ecabc-111">Si une table MFT prend en charge Direct3D 11, cet attribut fournit un indicateur à la MFT lors de l’allocation des surfaces Microsoft Direct3D pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="ecabc-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="ecabc-112">Définissez l’attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="ecabc-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="ecabc-113">Appelez [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) pour accéder au magasin d’attributs MFT.</span><span class="sxs-lookup"><span data-stu-id="ecabc-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="ecabc-114">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ecabc-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="ecabc-115">Le pipeline Media Foundation définit l’attribut avant le démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="ecabc-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="ecabc-116">La table MFT doit tenter d’honorer le paramètre lorsqu’il alloue des surfaces.</span><span class="sxs-lookup"><span data-stu-id="ecabc-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="ecabc-117">Si ce n’est pas possible, la table MFT peut ignorer l’attribut, au lieu d’échouer à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="ecabc-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="ecabc-118">En outre, si la table MFT requiert des surfaces Direct3D pour l’entrée, elle peut exposer cet attribut comme un indicateur pour la façon dont les surfaces d’entrée doivent être allouées.</span><span class="sxs-lookup"><span data-stu-id="ecabc-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="ecabc-119">Interrogez l’attribut comme suit :</span><span class="sxs-lookup"><span data-stu-id="ecabc-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="ecabc-120">Appelez [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) pour accéder aux attributs du flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ecabc-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="ecabc-121">Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ecabc-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="ecabc-122">Allocateur d’échantillon</span><span class="sxs-lookup"><span data-stu-id="ecabc-122">Sample Allocator</span></span>

<span data-ttu-id="ecabc-123">Cet attribut peut être défini sur l’allocateur d’échantillon vidéo, dans la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="ecabc-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecabc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecabc-124">Requirements</span></span>



| <span data-ttu-id="ecabc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecabc-125">Requirement</span></span> | <span data-ttu-id="ecabc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecabc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecabc-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecabc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ecabc-128">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ecabc-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ecabc-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecabc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ecabc-130">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ecabc-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ecabc-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecabc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecabc-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecabc-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecabc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecabc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecabc-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecabc-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
