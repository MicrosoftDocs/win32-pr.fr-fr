---
description: Crée une interface de jeu d’animations à clé ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: D3DXCreateKeyframedAnimationSet, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4fbfb31b712e1521930fa468bae315a443105f3a6bc0863fe3267f9586f874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804565"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>D3DXCreateKeyframedAnimationSet fonction)

Crée une interface de jeu d’animations à clé [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’ensemble d’animations.

</dd> <dt>

*TicksPerSecond* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Nombre de battements d’image clé qui s’écoulent par seconde.

</dd> <dt>

*Lecture* \[ dans\]
</dt> <dd>

Type : **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**

Type de la boucle de lecture du jeu d’animations. Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

*NumAnimations* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de jeux d’animations de mise à l’échelle, de rotation et de translation (SRT).

</dd> <dt>

*NumCallbackKeys* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clés de rappel.

</dd> <dt>

*pCallKeys* \[ dans\]
</dt> <dd>

Type : **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***

Pointeur vers une structure de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) qui stocke les données de rappel de l’utilisateur.

</dd> <dt>

*ppAnimationSet* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Adresse d’un pointeur vers la clé [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) de l’interface de jeu d’animations.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
