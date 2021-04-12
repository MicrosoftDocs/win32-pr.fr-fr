---
description: Spécifie si le moteur de capture utilise l’accélération vidéo DirectX (DXVA) pour le décodage vidéo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Attribut MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318550"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="3afe4-103">\_Désactiver l' \_ \_ \_ attribut DXVA du moteur de capture MF</span><span class="sxs-lookup"><span data-stu-id="3afe4-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="3afe4-104">Spécifie si le moteur de capture utilise l’accélération vidéo DirectX (DXVA) pour le décodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="3afe4-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="3afe4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3afe4-105">Data type</span></span>

<span data-ttu-id="3afe4-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3afe4-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3afe4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3afe4-107">Remarks</span></span>

<span data-ttu-id="3afe4-108">Cet attribut s’applique si les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="3afe4-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="3afe4-109">Le moteur de capture décode un flux vidéo compressé à partir du périphérique de capture (par exemple, si l’appareil de capture émet une vidéo H. 264).</span><span class="sxs-lookup"><span data-stu-id="3afe4-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="3afe4-110">Le décodeur vidéo prend en charge le décodage accéléré par le matériel à l’aide d’DXVA.</span><span class="sxs-lookup"><span data-stu-id="3afe4-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="3afe4-111">L’application utilise l’attribut de [ \_ \_ \_ \_ Gestionnaire D3D du moteur de capture MF](mf-capture-engine-d3d-manager.md) pour définir le gestionnaire de périphériques dxgi sur le moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="3afe4-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="3afe4-112">Dans le cas contraire, cet attribut est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3afe4-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="3afe4-113">Cet attribut permet à l’application de désactiver DXVA tout en décodant toujours les surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3afe4-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="3afe4-114">La valeur par défaut de cet attribut est **false**, ce qui signifie que le décodage DXVA est activé lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="3afe4-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="3afe4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3afe4-115">Requirements</span></span>



| <span data-ttu-id="3afe4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3afe4-116">Requirement</span></span> | <span data-ttu-id="3afe4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3afe4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3afe4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3afe4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3afe4-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3afe4-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3afe4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3afe4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3afe4-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3afe4-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3afe4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3afe4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3afe4-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3afe4-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3afe4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3afe4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3afe4-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3afe4-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3afe4-126">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="3afe4-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="3afe4-127">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3afe4-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




