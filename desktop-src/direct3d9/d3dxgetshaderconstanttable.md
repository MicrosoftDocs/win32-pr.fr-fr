---
description: 'Fonction D3DXGetShaderConstantTable : obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.'
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: D3DXGetShaderConstantTable, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTable
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a1375dfcf1bc75d6f2dee6f9923360b1b90fef01df5489f9f710175e7e1c2652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045007"
---
# <a name="d3dxgetshaderconstanttable-function"></a>D3DXGetShaderConstantTable fonction)

Obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
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

 *ppConstantTable* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retourne l’interface de table constante (consultez [**ID3DXConstantTable**](id3dxconstanttable.md)) qui gère la table constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Une table constante est générée par [**D3DXCompileShader**](d3dxcompileshader.md) et incorporée dans le corps du nuanceur. Si vous avez besoin d’un espace d’adressage virtuel supplémentaire, consultez [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
