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
# <a name="mft_message_set_d3d_manager"></a>\_ \_ Gestionnaire D3D des jeux de messages MFT \_ \_

Définit ou efface le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour DirectX Video ACCERERATION (DXVA).

## <a name="message-parameter"></a>Paramètre de message

Lors du démarrage de la diffusion en continu, le paramètre *ulParam* contient un pointeur **IUnknown** . La table MFT interroge ce pointeur sur l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) pour Direct3D 9 et l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) pour Direct3D 11. Lorsque la diffusion en continu s’arrête, le *ulParameter* contient la valeur **null**.

## <a name="remarks"></a>Notes

Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Ce message s’applique uniquement aux transformations vidéo. Le client ne doit pas envoyer ce message, sauf si la table MFT retourne la **valeur true** pour l’attribut prenant en charge la fonction [**\_ \_ D3D \_ MF sa**](mf-sa-d3d-aware-attribute.md) [ \_ \_ d3d11 \_](mf-sa-d3d11-aware.md) pour Direct3D 11.

N’envoyez pas ce message à une table MFT avec plusieurs sortis.

### <a name="implementation"></a>Implémentation

Une table MFT ne doit prendre en charge ce message que si la table MFT utilise l’accélération vidéo DirectX pour le traitement ou le décodage vidéo.

Si une table MFT prend en charge ce message, elle doit également implémenter la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) et retourner la valeur **true** pour l’attribut prenant en charge la méthode [**\_ \_ D3D \_ MF sa**](mf-sa-d3d-aware-attribute.md) (([MF \_ sa d3d11- \_ \_ Aware](mf-sa-d3d11-aware.md) pour Direct3D 11). Cet attribut informe le client que le client doit envoyer le message du **\_ \_ \_ \_ Gestionnaire D3D de l’ensemble de messages MFT** au MFT avant le début de la diffusion.

Si une table MFT ne prend pas en charge ce message, elle doit retourner **E \_ NOTIMPL** à partir de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Il s’agit d’une exception à la règle générale qu’une table MFT peut retourner **\_ OK** à partir de n’importe quel message qu’elle ignore.

Pour plus d’informations, voir [MFTS compatible Direct3D](direct3d-aware-mfts.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MFTs compatible Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_type de message MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




