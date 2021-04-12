---
description: Retourne le produit scalaire de deux quaternions.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: D3DXQuaternionDot, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323185"
---
# <a name="d3dxquaterniondot-function"></a>D3DXQuaternionDot fonction)

Retourne le produit scalaire de deux quaternions.

## <a name="syntax"></a>Syntaxe


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pQ1* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> <dt>

*pQ2* \[ dans\]
</dt> <dd>

Type : **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Pointeur vers une structure [**D3DXQUATERNION**](d3dxquaternion.md) source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **float**](../winprog/windows-data-types.md)**

Produit scalaire de deux quaternions.

## <a name="remarks"></a>Notes

Utilisez [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) pour toute entrée de Quaternion qui n’est pas déjà normalisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
