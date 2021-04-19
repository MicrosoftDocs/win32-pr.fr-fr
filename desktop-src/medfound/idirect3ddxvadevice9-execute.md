---
description: Effectue une opération de décodage DXVA (DirectX Video Acceleration).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9 :: Execute, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531894"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9 :: Execute, méthode

Effectue une opération de décodage DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FunctionNum* 
</dt> <dd>

**Valeur DWORD** qui contient un ou plusieurs numéros de fonction DXVA. Pour plus d’informations, reportez-vous à la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des données d’entrée pour l’opération de décodage. La signification de ces données dépend du type de surface et du numéro de fonction.

</dd> <dt>

*Inverser* 
</dt> <dd>

Taille des données d’entrée, en octets.

</dd> <dt>

*OutputData* 
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle l’accélérateur vidéo écrit des données de sortie.

</dd> <dt>

*En-dessous* 
</dt> <dd>

Taille de la mémoire tampon *OutputData* , en octets.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

Nombre d’éléments dans le tableau *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Pointeur vers un tableau de structures [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .

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

 

 
