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
# <a name="mf_sa_d3d_aware-attribute"></a>\_ \_ Attribut compatible D3D MF sa \_

Spécifie si une Media Foundation transformation (MFT) prend en charge l’accélération vidéo DirectX (DXVA). Cet attribut s’applique uniquement à la vidéo MFTs.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global de la table MFT. Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Cet attribut indique au client si la MFT peut utiliser la vidéo Direct3D 9 :

-   Si l’attribut est différent de zéro, le client peut attribuer à la MFT un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) avant le démarrage de la diffusion en continu. Pour ce faire, le client envoie le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) au MFT. Le client n’est pas obligé d’envoyer ce message.
-   Si cet attribut est égal à zéro (**false**), la table MFT ne prend pas en charge la vidéo Direct3D 9 et le client ne doit pas envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D de l’ensemble de messages MFT**](mft-message-set-d3d-manager.md) au MFT.

La valeur par défaut de cet attribut est **false**. Traiter cet attribut comme étant en lecture seule. Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.

Pour plus d’informations sur l’implémentation de cet attribut dans une table MFT personnalisée, voir [MFTS compatible Direct3D](direct3d-aware-mfts.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples

Le code suivant teste si une table MFT prend en charge DXVA.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs compatible Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_ \_ mode DXVA de topologie \_ MF](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




