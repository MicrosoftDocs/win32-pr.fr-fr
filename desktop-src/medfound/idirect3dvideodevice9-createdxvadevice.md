---
description: Crée un périphérique de décodage DXVA (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9 :: CreateDXVADevice, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555729"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>IDirect3DVideoDevice9 :: CreateDXVADevice, méthode

Crée un périphérique de décodage DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGuid* 
</dt> <dd>

Pointeur vers un GUID qui spécifie le périphérique à créer.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Pointeur vers une structure [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) qui spécifie le format de l’image non compressée.

</dd> <dt>

*pData* 
</dt> <dd>

Pointeur vers une structure **DXVA \_ ConnectMode** qui spécifie le mode DXVA et le profil restreint.

</dd> <dt>

*DataSize* 
</dt> <dd>

Taille de la structure **DXVA \_ ConnectMode** , en octets.

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) . L’appelant doit libérer l’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




