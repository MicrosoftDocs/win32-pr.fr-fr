---
description: Crée une interface de jeu d’animations à clé ID3DXCompressedAnimationSet qui stocke les données d’image clé dans un format compressé.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: D3DXCreateCompressedAnimationSet, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953878"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>D3DXCreateCompressedAnimationSet fonction)

Crée une interface de jeu d’animations à clé [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) qui stocke les données d’image clé dans un format compressé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
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

*pCompressedData* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Pointeur vers la mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’animation définie en tant que données compressées.

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

Type : **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Adresse d’un pointeur vers l’interface [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) qui stocke les données du jeu d’animations des clés dans un format compressé.

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

 

 
