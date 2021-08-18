---
description: 'ID3DXMATRIXStack :: GetTop, méthode (D3DX10. h)-récupère la matrice actuelle en haut de la pile.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack :: GetTop, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 340ea7ed85e05795dbc3949a29c5384871dfe840aa25ed4f9b2f07e1d4264de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852229"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>ID3DXMATRIXStack :: GetTop, méthode (D3DX10. h)

Récupère la matrice actuelle en haut de la pile.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Cette méthode retourne un pointeur vers une structure D3DXMATRIX représentant la matrice actuelle.

## <a name="remarks"></a>Remarques

Il n’est pas garanti que le pointeur D3DXMATRIX retourné par cette méthode soit valide après les opérations de pile suivantes.

Notez que cette méthode ne supprime pas la matrice actuelle du haut de la pile ; au lieu de cela, elle retourne simplement la matrice actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
