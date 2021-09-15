---
description: Active le décodage accéléré par le matériel à partir d’un appareil Direct3D 9, à l’aide de DirectX Video Acceleration (DXVA) version 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interface IDirect3DVideoDevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521473"
---
# <a name="idirect3dvideodevice9-interface"></a>Interface IDirect3DVideoDevice9

Active le décodage accéléré par le matériel à partir d’un appareil Direct3D 9, à l’aide de DirectX Video Acceleration (DXVA) version 1,0.

## <a name="when-to-use"></a>Quand l’utiliser

Cette interface n’est pas destinée à une utilisation générale des applications. les filtres de décodeur DirectShow doivent utiliser l’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , et non **IDirect3DVideoDevice9**. les broches d’entrée du filtre de mixage vidéo (VMR) et du filtre de Mixer de superposition exposent **IAMVideoAccelerator**.

## <a name="members"></a>Membres

L’interface **IDirect3DVideoDevice9** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DVideoDevice9** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirect3DVideoDevice9** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)                       | Crée un appareil de décodage DXVA.<br/>                                                                                         |
| [**CreateSurface**](idirect3dvideodevice9-createsurface.md)                             | Crée une surface compressée pour le décodage DXVA.<br/>                                                                        |
| [**GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.<br/>                                |
| [**GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)                               | Obtient une liste des profils DXVA pris en charge par le pilote d’affichage.<br/>                                             |
| [**GetDXVAInternalInfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Recherche la quantité de mémoire de travail allouée par la couche d’abstraction matérielle (HAL) pour son usage privé. <br/> |
| [**GetUncompressedDXVAFormats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil DXVA spécifié.<br/>                         |



 

## <a name="remarks"></a>Notes

Pour obtenir un pointeur vers cette interface, appelez **QueryInterface** sur un pointeur [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) ou [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) .

Cette interface prend en charge DXVA 1,0 uniquement. Elle ne prend pas en charge la 2,0 DXVA.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces vidéo Direct3D](direct3d-video-interfaces.md)
</dt> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Spécification 1,0 DXVA](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
