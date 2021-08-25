---
description: Retourne le nombre d’éléments dans la déclaration de vertex.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: D3DXGetDeclLength, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc6a44c73d9b7127bb382cfbf18587a84d8cc179feabf48da6e29b908204b1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857038"
---
# <a name="d3dxgetdecllength-function"></a>D3DXGetDeclLength fonction)

Retourne le nombre d’éléments dans la déclaration de vertex.

## <a name="syntax"></a>Syntaxe


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Pointeur vers la déclaration de vertex. Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments dans la déclaration de vertex.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
