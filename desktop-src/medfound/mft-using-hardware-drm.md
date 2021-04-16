---
description: Spécifie si le IMFTransform utilise le matériel DRM.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485345"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="353dd-103">MFT \_ utilisant \_ l' \_ attribut DRM matériel</span><span class="sxs-lookup"><span data-stu-id="353dd-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="353dd-104">Spécifie si le IMFTransform utilise le matériel DRM.</span><span class="sxs-lookup"><span data-stu-id="353dd-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="353dd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="353dd-105">Data type</span></span>

<span data-ttu-id="353dd-106">**UInt32** (traité comme **bool**)</span><span class="sxs-lookup"><span data-stu-id="353dd-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="353dd-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="353dd-107">Get/set</span></span>

<span data-ttu-id="353dd-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="353dd-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="353dd-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="353dd-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="353dd-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="353dd-110">Applies to</span></span>

[<span data-ttu-id="353dd-111">**IMTransfrom**</span><span class="sxs-lookup"><span data-stu-id="353dd-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="353dd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="353dd-112">Remarks</span></span>

<span data-ttu-id="353dd-113">Si un Decrypter MFT spécifie que cet attribut a la valeur 1, il utilise le service DRM matériel.</span><span class="sxs-lookup"><span data-stu-id="353dd-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="353dd-114">Si un Decrypter MFT spécifie que cet attribut a la valeur 0, il n’utilise pas de DRM matériel.</span><span class="sxs-lookup"><span data-stu-id="353dd-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="353dd-115">Si un Decrypter MFT ne spécifie pas cet attribut ou le spécifie avec une valeur différente, alors il n’est pas (ou n’est pas possible) d’indiquer s’il utilise la DRM matérielle.</span><span class="sxs-lookup"><span data-stu-id="353dd-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="353dd-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="353dd-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="353dd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="353dd-117">Requirements</span></span>



| <span data-ttu-id="353dd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="353dd-118">Requirement</span></span> | <span data-ttu-id="353dd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="353dd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="353dd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="353dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="353dd-121">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="353dd-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="353dd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="353dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="353dd-123">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="353dd-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="353dd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="353dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="353dd-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="353dd-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353dd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="353dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353dd-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="353dd-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="353dd-128">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="353dd-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




