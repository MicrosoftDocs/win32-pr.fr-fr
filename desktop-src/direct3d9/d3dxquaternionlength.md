---
description: Retourne la longueur d’un Quaternion.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: D3DXQuaternionLength, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21589f6e470c1f23bd537b2983c7073a3f8c29866534418077018f616ca6b25f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044687"
---
# <a name="d3dxquaternionlength-function"></a>D3DXQuaternionLength fonction)

Retourne la longueur d’un Quaternion.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PQ* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers la structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Longueur du Quaternion.

## <a name="remarks"></a>Remarques

Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
