---
description: Obtient la sémantique pour tous les éléments de sortie du nuanceur.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: D3DXGetShaderOutputSemantics, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fda2c2ac5e331874448e251b14654ba06df33bea6557f75957f8955387b2591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986789"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>D3DXGetShaderOutputSemantics fonction)

Obtient la sémantique pour tous les éléments de sortie du nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction de nuanceur DWORD.

</dd> <dt>

*pSemantics* \[ dans\]
</dt> <dd>

Type : **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Pointeur vers un tableau de structures [**D3DXSEMANTIC**](d3dxsemantic.md) . La fonction remplit ce tableau avec la sémantique pour chaque élément de sortie référencé par le nuanceur. Ce tableau est supposé contenir au moins des éléments MAXD3DDECLLENGTH. Toutefois, l’appel de **D3DXGetShaderOutputSemantics** avec PSemantics = **null** retourne le nombre d’éléments nécessaires pour pCount.

</dd> <dt>

*pCount* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Retourne le nombre d’éléments dans pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
