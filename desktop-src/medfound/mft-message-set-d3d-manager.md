---
description: Définit ou efface le Gestionnaire de périphériques Direct3D pour DirectX Video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524989"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="9a42b-103">\_ \_ Gestionnaire D3D des jeux de messages MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="9a42b-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="9a42b-104">Définit ou efface le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour DirectX Video ACCERERATION (DXVA).</span><span class="sxs-lookup"><span data-stu-id="9a42b-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="9a42b-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="9a42b-105">Message Parameter</span></span>

<span data-ttu-id="9a42b-106">Lors du démarrage de la diffusion en continu, le paramètre *ulParam* contient un pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9a42b-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="9a42b-107">La table MFT interroge ce pointeur sur l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pour Direct3D 9 et l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) pour Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="9a42b-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="9a42b-108">Lorsque la diffusion en continu s’arrête, le *ulParameter* contient la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="9a42b-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a42b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9a42b-109">Remarks</span></span>

<span data-ttu-id="9a42b-110">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="9a42b-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="9a42b-111">Ce message s’applique uniquement aux transformations vidéo.</span><span class="sxs-lookup"><span data-stu-id="9a42b-111">This message applies only to video transforms.</span></span> <span data-ttu-id="9a42b-112">Le client ne doit pas envoyer ce message, sauf si la table MFT retourne la **valeur true** pour l’attribut prenant en charge la fonction [**\_ \_ D3D \_ MF sa**](mf-sa-d3d-aware-attribute.md) [ \_ \_ d3d11 \_](mf-sa-d3d11-aware.md) pour Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="9a42b-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="9a42b-113">N’envoyez pas ce message à une table MFT avec plusieurs sortis.</span><span class="sxs-lookup"><span data-stu-id="9a42b-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="9a42b-114">Implémentation</span><span class="sxs-lookup"><span data-stu-id="9a42b-114">Implementation</span></span>

<span data-ttu-id="9a42b-115">Une table MFT ne doit prendre en charge ce message que si la table MFT utilise l’accélération vidéo DirectX pour le traitement ou le décodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="9a42b-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="9a42b-116">Si une table MFT prend en charge ce message, elle doit également implémenter la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) et retourner la valeur **true** pour l’attribut prenant en charge la méthode [**\_ \_ D3D \_ MF sa**](mf-sa-d3d-aware-attribute.md) (([MF \_ sa d3d11- \_ \_ Aware](mf-sa-d3d11-aware.md) pour Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="9a42b-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="9a42b-117">Cet attribut informe le client que le client doit envoyer le message du **\_ \_ \_ \_ Gestionnaire D3D de l’ensemble de messages MFT** au MFT avant le début de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="9a42b-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="9a42b-118">Si une table MFT ne prend pas en charge ce message, elle doit retourner **E \_ NOTIMPL** à partir de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="9a42b-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="9a42b-119">Il s’agit d’une exception à la règle générale qu’une table MFT peut retourner **\_ OK** à partir de n’importe quel message qu’elle ignore.</span><span class="sxs-lookup"><span data-stu-id="9a42b-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="9a42b-120">Pour plus d’informations, voir [MFTS compatible Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="9a42b-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a42b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a42b-121">Requirements</span></span>



| <span data-ttu-id="9a42b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a42b-122">Requirement</span></span> | <span data-ttu-id="9a42b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a42b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a42b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a42b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9a42b-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a42b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a42b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a42b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9a42b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a42b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9a42b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a42b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a42b-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a42b-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a42b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a42b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a42b-131">MFTs compatible Direct3D</span><span class="sxs-lookup"><span data-stu-id="9a42b-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="9a42b-132">Prise en charge de DXVA 2,0 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a42b-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9a42b-133">Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a42b-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="9a42b-134">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="9a42b-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




