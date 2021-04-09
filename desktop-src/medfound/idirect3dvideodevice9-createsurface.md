---
description: Crée une surface compressée pour le décodage DXVA (DirectX Video Acceleration).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9 :: CreateSurface, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115211"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9 :: CreateSurface, méthode

Crée une surface compressée pour le décodage DXVA (DirectX Video Acceleration).

Pour connaître les exigences de surface, appelez [**IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) et examinez les structures [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) retournées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Width* 
</dt> <dd>

Largeur de la surface, en pixels. Affectez à ce paramètre la valeur **DXVACompBufferInfo. WidthToCreate**.

</dd> <dt>

*Height* 
</dt> <dd>

Hauteur de la surface, en pixels. Affectez à ce paramètre la valeur **DXVACompBufferInfo. HeightToCreate**.

</dd> <dt>

*Tous* 
</dt> <dd>

Nombre de mémoires tampons d’arrière-plan. Ce paramètre peut être égal à zéro.

</dd> <dt>

*Format* 
</dt> <dd>

Format de pixel, spécifié en tant que valeur **D3DFORMAT** . Affectez à ce paramètre la valeur **DXVACompBufferInfo. format**.

</dd> <dt>

*Pool* 
</dt> <dd>

Pool de mémoire dans lequel créer la surface, spécifié comme valeur **D3DPOOL** . Affectez à ce paramètre la valeur **DXVACompBufferInfo. pool**.

</dd> <dt>

*Utilisation* 
</dt> <dd>

**Or au niveau du** bit d’une ou plusieurs constantes **D3DUSAGE** . Affectez à ce paramètre la valeur **DXVACompBufferInfo. usage**.

</dd> <dt>

*ppSurface* 
</dt> <dd>

Reçoit un pointeur vers l’interface **IDirect3DSurface9** . L’appelant doit libérer l’interface.

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Réservé. Affectez la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




