---
description: Désassemblez un effet.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: D3DXDisassembleEffect, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524859"
---
# <a name="d3dxdisassembleeffect-function"></a>D3DXDisassembleEffect fonction)

Désassemblez un effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEffect* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)**

Pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) qui contient l’effet.

</dd> <dt>

*EnableColorCode* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Activez le codage en couleurs pour faciliter la lecture du code machine.

</dd> <dt>

*ppDisassembly* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon contenant le nuanceur désassemblé. Consultez [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Effect](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
