---
description: 'Fonction D3DXGetShaderConstantTableEx : obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: D3DXGetShaderConstantTableEx, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c3d54a7fa314fe2987d5e1004f7dcd8302753dbb3f0e493d838e3d6407d8db0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027429"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>D3DXGetShaderConstantTableEx fonction)

Obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction DWORD.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Utilisez l' \_ indicateur D3DXCONSTTABLE LARGEADDRESSAWARE pour accéder à un espace d’adressage virtuel de 4 Go maximum (au lieu de 2 Go par défaut). Si vous n’avez pas besoin de l’espace d’adressage virtuel supplémentaire, utilisez [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).

</dd> <dt>

 *ppConstantTable* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retourne l’interface de table constante (consultez [**ID3DXConstantTable**](id3dxconstanttable.md)) qui gère la table constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Une table constante est générée par [**D3DXCompileShader**](d3dxcompileshader.md) et incorporée dans le corps du nuanceur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
