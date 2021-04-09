---
description: Spécifie le nombre de points de terminaison de streaming et le nombre de flux pris en charge pour un encodeur H. 264 UVC.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: Attribut MF_MT_H264_SIMULCAST_SUPPORT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862750"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a><span data-ttu-id="a310e-103">\_Attribut de \_ \_ \_ prise en charge d’MF MT H264 – simultané</span><span class="sxs-lookup"><span data-stu-id="a310e-103">MF\_MT\_H264\_SIMULCAST\_SUPPORT attribute</span></span>

<span data-ttu-id="a310e-104">Spécifie le nombre de points de terminaison de streaming et le nombre de flux pris en charge pour un encodeur H. 264 UVC.</span><span class="sxs-lookup"><span data-stu-id="a310e-104">Specifies the number of streaming endpoints and the number of supported streams for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="a310e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a310e-105">Data type</span></span>

<span data-ttu-id="a310e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a310e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a310e-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="a310e-107">Get/set</span></span>

<span data-ttu-id="a310e-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a310e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a310e-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a310e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a310e-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="a310e-110">Applies to</span></span>

[<span data-ttu-id="a310e-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a310e-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="a310e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a310e-112">Remarks</span></span>

<span data-ttu-id="a310e-113">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="a310e-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="a310e-114">La valeur correspond au champ **bSimulcastSupport** dans le descripteur de format vidéo 1,5 UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="a310e-114">The value corresponds to the **bSimulcastSupport** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="a310e-115">Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="a310e-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a310e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a310e-116">Requirements</span></span>



| <span data-ttu-id="a310e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a310e-117">Requirement</span></span> | <span data-ttu-id="a310e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a310e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a310e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a310e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a310e-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a310e-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a310e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a310e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a310e-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="a310e-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a310e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a310e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a310e-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a310e-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a310e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a310e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a310e-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a310e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a310e-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="a310e-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




