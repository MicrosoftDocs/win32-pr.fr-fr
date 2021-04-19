---
description: Commence le traitement pour créer une image décodée.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9 :: BeginFrame, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518203"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>IDirect3DDXVADevice9 :: BeginFrame, méthode

Commence le traitement pour créer une image décodée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDstSurface* 
</dt> <dd>

Pointeur vers l’interface **IDirect3DSurface9** de la surface de destination non compressée.

</dd> <dt>

*SizeInputData* 
</dt> <dd>

Taille de la mémoire tampon spécifiée par *pInputData*, en octets. La valeur doit être 2.

</dd> <dt>

*pInputData* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des données pour l’accélérateur vidéo. Cette mémoire tampon doit contenir l’index de frame de base zéro, spécifié sous la forme d’une valeur de **mot** .

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

Taille de la mémoire tampon spécifiée par *pOutputData*, en octets. La valeur doit être égale à zéro.

</dd> <dt>

*pOutputData* 
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle l’accélérateur vidéo peut écrire. Affectez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Pour chaque appel à **BeginFrame**, le décodeur doit effectuer un appel correspondant à [**IDirect3DDXVADevice9 :: EndFrame**](idirect3ddxvadevice9-endframe.md).

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

 

 




