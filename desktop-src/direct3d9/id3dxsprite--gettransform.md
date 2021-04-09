---
description: Obtient la transformation de sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'ID3DXSprite :: GetTransform, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043124"
---
# <a name="id3dxspritegettransform-method"></a>ID3DXSprite :: GetTransform, méthode

Obtient la transformation de sprite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTransform* \[ dans\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation du sprite à partir de l’espace universel d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




