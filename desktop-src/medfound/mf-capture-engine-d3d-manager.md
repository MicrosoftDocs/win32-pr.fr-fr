---
description: Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: Attribut MF_CAPTURE_ENGINE_D3D_MANAGER (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113683"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="124cc-103">\_Attribut du \_ \_ Gestionnaire D3D du moteur de capture MF \_</span><span class="sxs-lookup"><span data-stu-id="124cc-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="124cc-104">Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="124cc-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="124cc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="124cc-105">Data type</span></span>

<span data-ttu-id="124cc-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="124cc-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="124cc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="124cc-107">Remarks</span></span>

<span data-ttu-id="124cc-108">La valeur de cet attribut est un pointeur vers l’interface [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="124cc-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="124cc-109">Cet attribut permet au moteur de capture d’allouer des images vidéo à l’aide de surfaces DXGI et d’utiliser l’accélération matérielle pour le décodage et le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="124cc-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="124cc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="124cc-110">Requirements</span></span>



| <span data-ttu-id="124cc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="124cc-111">Requirement</span></span> | <span data-ttu-id="124cc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="124cc-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="124cc-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="124cc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="124cc-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="124cc-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="124cc-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="124cc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="124cc-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="124cc-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="124cc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="124cc-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="124cc-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="124cc-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124cc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="124cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124cc-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="124cc-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="124cc-121">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="124cc-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="124cc-122">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="124cc-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




