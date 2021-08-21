---
description: Obtient la taille du correctif triangulaire.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: D3DXTriPatchSize, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 54eba8131d59b9d1e68526cd26bb74b497bcec21fcbffdb4229678f166646806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298241"
---
# <a name="d3dxtripatchsize-function"></a>D3DXTriPatchSize fonction)

Obtient la taille du correctif triangulaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfNumSegs* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Nombre de segments par périphérie à paver.

</dd> <dt>

*pdwTriangles* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur DWORD qui contient le nombre de triangles dans le correctif.

</dd> <dt>

*pdwVertices* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur DWORD qui contient le nombre de vertex dans le correctif triangulaire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
