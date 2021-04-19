---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge l’accélération vidéo DirectX (DXVA). Cet attribut s’applique uniquement à la vidéo MFTs.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Attribut MF_SA_D3D_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524311"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="b6663-104">\_ \_ Attribut compatible D3D MF sa \_</span><span class="sxs-lookup"><span data-stu-id="b6663-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="b6663-105">Spécifie si une Media Foundation transformation (MFT) prend en charge l’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="b6663-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="b6663-106">Cet attribut s’applique uniquement à la vidéo MFTs.</span><span class="sxs-lookup"><span data-stu-id="b6663-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6663-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6663-107">Data type</span></span>

<span data-ttu-id="b6663-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6663-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b6663-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b6663-109">Remarks</span></span>

<span data-ttu-id="b6663-110">Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="b6663-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="b6663-111">Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b6663-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b6663-112">Cet attribut indique au client si la MFT peut utiliser la vidéo Direct3D 9 :</span><span class="sxs-lookup"><span data-stu-id="b6663-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="b6663-113">Si l’attribut est différent de zéro, le client peut attribuer à la MFT un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) avant le démarrage de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b6663-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="b6663-114">Pour ce faire, le client envoie le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) au MFT.</span><span class="sxs-lookup"><span data-stu-id="b6663-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="b6663-115">Le client n’est pas obligé d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="b6663-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="b6663-116">Si cet attribut est égal à zéro (**false**), la table MFT ne prend pas en charge la vidéo Direct3D 9 et le client ne doit pas envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D de l’ensemble de messages MFT**](mft-message-set-d3d-manager.md) au MFT.</span><span class="sxs-lookup"><span data-stu-id="b6663-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="b6663-117">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="b6663-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="b6663-118">Traiter cet attribut comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b6663-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="b6663-119">Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="b6663-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="b6663-120">Pour plus d’informations sur l’implémentation de cet attribut dans une table MFT personnalisée, voir [MFTS compatible Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="b6663-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="b6663-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b6663-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="b6663-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="b6663-122">Examples</span></span>

<span data-ttu-id="b6663-123">Le code suivant teste si une table MFT prend en charge DXVA.</span><span class="sxs-lookup"><span data-stu-id="b6663-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="b6663-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6663-124">Requirements</span></span>



| <span data-ttu-id="b6663-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6663-125">Requirement</span></span> | <span data-ttu-id="b6663-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6663-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6663-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6663-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b6663-128">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b6663-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="b6663-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6663-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b6663-130">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b6663-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b6663-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6663-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6663-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6663-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6663-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6663-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6663-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6663-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6663-135">MFTs compatible Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6663-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="b6663-136">Prise en charge de DXVA 2,0 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6663-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b6663-137">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6663-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="b6663-138">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="b6663-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6663-139">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b6663-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b6663-140">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b6663-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b6663-141">\_ \_ mode DXVA de topologie \_ MF</span><span class="sxs-lookup"><span data-stu-id="b6663-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




