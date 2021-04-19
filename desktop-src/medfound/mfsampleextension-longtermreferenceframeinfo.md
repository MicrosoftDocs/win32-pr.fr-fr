---
description: Spécifie les informations de trame de référence à long terme et est retourné sur l’exemple de sortie.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Attribut MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522284"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="bf19b-103">\_Attribut MFSampleExtension LongTermReferenceFrameInfo</span><span class="sxs-lookup"><span data-stu-id="bf19b-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="bf19b-104">Spécifie les informations de trame de référence à long terme et est retourné sur l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="bf19b-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="bf19b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="bf19b-105">Data type</span></span>

<span data-ttu-id="bf19b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bf19b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bf19b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bf19b-107">Remarks</span></span>

<span data-ttu-id="bf19b-108">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="bf19b-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="bf19b-109">Les encodeurs retournent cet attribut sur l’exemple de sortie lorsque l’application contrôle les frames LTR, qui est spécifié par [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="bf19b-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="bf19b-110">MFSampleExtension \_ LongTermReferenceFrameInfo retourne jusqu’à deux champs.</span><span class="sxs-lookup"><span data-stu-id="bf19b-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="bf19b-111">Le premier champ, bits \[ 0.. 15 \] , est *LongTermFrameIdx* associé au frame de sortie s’il est marqué comme cadre LTR.</span><span class="sxs-lookup"><span data-stu-id="bf19b-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="bf19b-112">La première valeur est 0xFFFF, si ce frame de sortie est une trame de référence à bref terme ou un frame non-référence.</span><span class="sxs-lookup"><span data-stu-id="bf19b-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="bf19b-113">Le deuxième champ, bits \[ 16.. 31 \] , est une image bitmap composée de *MaxNumLTRFrames* de nombreux bits qui indiquent le ou les frames LTR utilisés pour l’encodage de ce frame de sortie, à partir du bit 16.</span><span class="sxs-lookup"><span data-stu-id="bf19b-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="bf19b-114">Le reste de bits doit être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="bf19b-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="bf19b-115">La deuxième valeur est 0 si cette trame de sortie n’est pas encodée à l’aide d’une trame LTR.</span><span class="sxs-lookup"><span data-stu-id="bf19b-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="bf19b-116">*MaxNumLTRFrames* est le nombre maximal de frames LTR définis via [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="bf19b-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf19b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf19b-117">Requirements</span></span>



| <span data-ttu-id="bf19b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf19b-118">Requirement</span></span> | <span data-ttu-id="bf19b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf19b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf19b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf19b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf19b-121">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf19b-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="bf19b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf19b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf19b-123">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf19b-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bf19b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf19b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf19b-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf19b-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf19b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf19b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf19b-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf19b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




