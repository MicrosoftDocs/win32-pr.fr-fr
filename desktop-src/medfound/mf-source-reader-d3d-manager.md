---
description: Contient un pointeur vers le Gestionnaire de périphériques Microsoft Direct3D pour le lecteur source.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Attribut MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865578"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="7ed50-103">\_Attribut du \_ \_ Gestionnaire D3D du lecteur source MF \_</span><span class="sxs-lookup"><span data-stu-id="7ed50-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="7ed50-104">Contient un pointeur vers le [Gestionnaire de périphériques Microsoft Direct3D](direct3d-device-manager.md) pour le [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="7ed50-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="7ed50-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ed50-105">Data type</span></span>

<span data-ttu-id="7ed50-106">**IDirect3DDeviceManager9 \* ou IMFDXGIDeviceManager \*** stocké sous la forme \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="7ed50-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="7ed50-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7ed50-107">Get/set</span></span>

<span data-ttu-id="7ed50-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="7ed50-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="7ed50-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="7ed50-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ed50-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7ed50-110">Remarks</span></span>

<span data-ttu-id="7ed50-111">La valeur de cet attribut peut être un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ou un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span><span class="sxs-lookup"><span data-stu-id="7ed50-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="7ed50-112">Utilisez cet attribut pour fournir un appareil Direct3D pour tous les décodeurs vidéo chargés par le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="7ed50-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="7ed50-113">Si vous définissez cet attribut et que le décodeur prend en charge l’accélération vidéo Microsoft DirectX (DXVA), le lecteur source utilise le périphérique Direct3D pour allouer des mémoires tampons vidéo.</span><span class="sxs-lookup"><span data-stu-id="7ed50-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="7ed50-114">Ces mémoires tampons sont compatibles avec le processeur vidéo DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="7ed50-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="7ed50-115">(Voir [traitement vidéo DXVA](dxva-video-processing.md).)</span><span class="sxs-lookup"><span data-stu-id="7ed50-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="7ed50-116">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ed50-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="7ed50-117">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="7ed50-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="7ed50-118">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7ed50-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="7ed50-119">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="7ed50-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="7ed50-120">En général, vous définissez cet attribut si vous utilisez le lecteur source pour obtenir des trames vidéo décodées et que vous utilisez Direct3D pour afficher les frames.</span><span class="sxs-lookup"><span data-stu-id="7ed50-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="7ed50-121">La définition de cet attribut permet au décodeur d’utiliser DXVA.</span><span class="sxs-lookup"><span data-stu-id="7ed50-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="7ed50-122">Vous ne définissez pas cet attribut si :</span><span class="sxs-lookup"><span data-stu-id="7ed50-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="7ed50-123">Vous utilisez le lecteur source pour traiter uniquement les données audio et non vidéo.</span><span class="sxs-lookup"><span data-stu-id="7ed50-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="7ed50-124">Vous obtenez une vidéo compressée à partir du lecteur source.</span><span class="sxs-lookup"><span data-stu-id="7ed50-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="7ed50-125">Dans ce cas, le lecteur source ne crée pas de décodeur.</span><span class="sxs-lookup"><span data-stu-id="7ed50-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed50-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ed50-126">Requirements</span></span>



| <span data-ttu-id="7ed50-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ed50-127">Requirement</span></span> | <span data-ttu-id="7ed50-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed50-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed50-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed50-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed50-130">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7ed50-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7ed50-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed50-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed50-132">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7ed50-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7ed50-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ed50-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed50-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed50-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed50-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ed50-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed50-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ed50-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ed50-137">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="7ed50-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="7ed50-138">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="7ed50-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




