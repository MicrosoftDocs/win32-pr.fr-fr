---
description: Termine le traitement pour créer une image décodée.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9 :: EndFrame, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531912"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>IDirect3DDXVADevice9 :: EndFrame, méthode

Termine le traitement pour créer une image décodée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SizeMiscData* 
</dt> <dd>

Taille de la mémoire tampon spécifiée par *pMiscData*, en octets. La valeur doit être 2.

</dd> <dt>

*pMiscData* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des données pour l’accélérateur vidéo. Cette mémoire tampon doit contenir le même index de frames que celui qui a été passé à la méthode [**IDirect3DDXVADevice9 :: BeginFrame**](idirect3ddxvadevice9-beginframe.md) dans le paramètre *pInputData* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




