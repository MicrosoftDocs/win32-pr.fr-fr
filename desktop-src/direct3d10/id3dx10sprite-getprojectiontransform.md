---
description: Obtient la matrice de projection Sprite qui est appliquée à tous les sprites.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'ID3DX10Sprite :: GetProjectionTransform, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5c3f5b0a0dc60316398575855c79bdb8ac9b7113f953af75489d5b65d9ff8fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301965"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>ID3DX10Sprite :: GetProjectionTransform, méthode

Obtient la matrice de projection Sprite qui est appliquée à tous les sprites.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProjectionTransform* \[ à\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Pointeur vers un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) qui sera défini sur la matrice de projection du sprite.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
