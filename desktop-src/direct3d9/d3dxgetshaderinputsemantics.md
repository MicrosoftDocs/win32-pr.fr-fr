---
description: Obtient la sémantique pour les entrées du nuanceur. Utilisez cette méthode pour déterminer le format de vertex d’entrée.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: D3DXGetShaderInputSemantics, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc5818d8f41bcfa9be9114ac7d131d11ff0d1dded00c191031c325ca7aeb50d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791829"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>D3DXGetShaderInputSemantics fonction)

Obtient la sémantique pour les entrées du nuanceur. Utilisez cette méthode pour déterminer le format de vertex d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetShaderInputSemantics(
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

Pointeur vers un tableau de structures [**D3DXSEMANTIC**](d3dxsemantic.md) . La fonction remplit ce tableau avec la sémantique de chaque élément d’entrée référencé par le nuanceur. Ce tableau est supposé contenir au moins des éléments MAXD3DDECLLENGTH. Toutefois, l’appel de **D3DXGetShaderInputSemantics** avec PSemantics = **null** retourne le nombre d’éléments nécessaires pour pCount.

</dd> <dt>

*pCount* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Retourne le nombre d’éléments dans pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Utilisez **D3DXGetShaderInputSemantics** pour retourner une liste des sémantiques d’entrée requises par le nuanceur. Il s’agit de la façon de déterminer le format de vertex d’entrée pour un nuanceur HLSL (High-Level Shader Language). Si le nuanceur a des entrées supplémentaires pour lesquelles votre déclaration de vertex est manquante, vous pouvez créer un flux de vertex supplémentaire avec un Stride de 0 qui contient les composants manquants avec des valeurs par défaut. Par exemple, cette technique peut être utilisée pour fournir la couleur de vertex par défaut pour les modèles qui ne le spécifient pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
