---
description: Spécifie la taille de la mémoire tampon utilisée pendant l’encodage. Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propriété AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109667"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="fb2f1-104">Propriété AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="fb2f1-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="fb2f1-105">Spécifie la taille de la mémoire tampon utilisée pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="fb2f1-106">Cette propriété s’applique uniquement aux modes d’encodage à vitesse de transmission constante (CBR) et à vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="fb2f1-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="fb2f1-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fb2f1-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="fb2f1-108">Data type</span></span>

<span data-ttu-id="fb2f1-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fb2f1-110">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="fb2f1-110">Property GUID</span></span>

<span data-ttu-id="fb2f1-111">**CODECAPI \_ AVEncCommonBufferSize**</span><span class="sxs-lookup"><span data-stu-id="fb2f1-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="fb2f1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb2f1-112">Property value</span></span>

<span data-ttu-id="fb2f1-113">Cette propriété a une plage de valeurs linéaire.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-113">This property has a linear range of values.</span></span> <span data-ttu-id="fb2f1-114">Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="fb2f1-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="fb2f1-115">Les plages de paramètres ne sont pas prises en charge pour les encodeurs de caméra H. 264 UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2f1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fb2f1-116">Remarks</span></span>

<span data-ttu-id="fb2f1-117">Pour certains formats vidéo, la taille de la mémoire tampon est spécifiée en bits et, pour d’autres, elle est spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="fb2f1-118">Consultez les remarques ci-dessous pour obtenir des informations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="fb2f1-119">Pour la vidéo MPEG, cette propriété définit la taille de la mémoire tampon du vérificateur de mémoire tampon vidéo (VBV).</span><span class="sxs-lookup"><span data-stu-id="fb2f1-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="fb2f1-120">La taille de la mémoire tampon est en bits.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="fb2f1-121">Pour la vidéo H. 264 et Windows Media Video, la propriété définit la taille du décodeur de référence hypothétique (découverte du domaine).</span><span class="sxs-lookup"><span data-stu-id="fb2f1-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="fb2f1-122">La taille de la mémoire tampon est en octets.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="fb2f1-123">Pour les caméras de codage UVC 1,5 H264 –, la valeur CPB envoyée à l’encodeur de l’appareil photo doit être alignée sur 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="fb2f1-124">La taille de la mémoire tampon est en octets.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="fb2f1-125">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="fb2f1-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2f1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb2f1-126">Requirements</span></span>



| <span data-ttu-id="fb2f1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb2f1-127">Requirement</span></span> | <span data-ttu-id="fb2f1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb2f1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2f1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2f1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2f1-130">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fb2f1-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fb2f1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2f1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2f1-132">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="fb2f1-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fb2f1-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb2f1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2f1-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2f1-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb2f1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb2f1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2f1-136">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="fb2f1-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fb2f1-137">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fb2f1-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

