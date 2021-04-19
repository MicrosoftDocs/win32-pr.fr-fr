---
description: Retourne la taille d’un vertex à partir de la déclaration de vertex.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: D3DXGetDeclVertexSize, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524856"
---
# <a name="d3dxgetdeclvertexsize-function"></a>D3DXGetDeclVertexSize fonction)

Retourne la taille d’un vertex à partir de la déclaration de vertex.

## <a name="syntax"></a>Syntaxe


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Pointeur vers la déclaration de vertex. Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*Flux* \[ de dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de flux de base zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille de la déclaration de vertex, en octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
