---
description: Obtenir les noms d’échantillonneur référencés dans un nuanceur.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: D3DXGetShaderSamplers, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519269"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers fonction)

Obtenir les noms d’échantillonneur référencés dans un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction de nuanceur DWORD.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de LPCSTRs. La fonction remplit ce tableau avec des pointeurs vers les noms d’échantillonneurs contenus dans *pFunction*. La taille de tableau maximale est le nombre maximal de registres d’échantillonnage (16 pour vs \_ 3 \_ 0 et PS \_ 3 \_ 0).

Pour déterminer le nombre d’échantillonneurs utilisés, consultez *pCount* après avoir appelé **D3DXGetShaderSamplers** avec pSamplers = **null**.

</dd> <dt>

*pCount* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Retourne le nombre d’échantillonneurs référencés par le nuanceur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
