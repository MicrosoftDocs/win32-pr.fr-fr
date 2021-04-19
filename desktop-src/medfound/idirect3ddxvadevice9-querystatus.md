---
description: Interroge l’État lecture/écriture d’une surface de décodage DXVA (DirectX Video Acceleration).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9 :: QueryStatus, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518982"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>IDirect3DDXVADevice9 :: QueryStatus, méthode

Interroge l’État lecture/écriture d’une surface de décodage DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSurface* 
</dt> <dd>

Pointeur vers l’interface **IDirect3DSurface9** de la surface à interroger.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Spécifie le type de requête à effectuer.



| Valeur                                                                                                                             | Signification                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Teste si la surface peut être utilisée en toute sécurité pour l’écriture.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Teste si la surface peut être utilisée en toute sécurité pour la lecture.<br/> |



 

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

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




