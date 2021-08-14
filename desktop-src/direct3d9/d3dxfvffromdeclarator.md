---
description: Retourne un code de format de vertex flexible (Commission) à partir d’un déclarateur.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: D3DXFVFFromDeclarator, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f9bad9968a52fb6c3b11de96936f48e432bd038e172318cb52f21fad4b08ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525646"
---
# <a name="d3dxfvffromdeclarator-function"></a>D3DXFVFFromDeclarator fonction)

Retourne un code de format de vertex flexible (Commission) à partir d’un déclarateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDeclaration* \[ dans\]
</dt> <dd>

Type : **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le code de la Commission.

</dd> <dt>

*pFVF* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur DWORD représentant la combinaison retournée de [D3DFVF](d3dfvf.md) qui décrit le format de vertex retourné par le déclarateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette fonction échoue pour tout déclarateur qui ne correspond pas directement à un prix de la Commission.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
