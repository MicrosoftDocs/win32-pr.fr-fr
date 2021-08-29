---
description: 'ID3DXMATRIXStack :: GetTop, méthode (D3dx9math. h)-récupère la matrice actuelle en haut de la pile.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack :: GetTop, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b2de5a846bdcc1296686011c8a176275a1c4a578bfbf2eff3a2c1ffe7af6efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095919"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>ID3DXMATRIXStack :: GetTop, méthode (D3dx9math. h)

Récupère la matrice actuelle en haut de la pile.

## <a name="syntax"></a>Syntaxe


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Cette méthode retourne un pointeur vers une structure [**D3DXMATRIX**](d3dxmatrix.md) représentant la matrice actuelle.

## <a name="remarks"></a>Remarques

Il n’est pas garanti que le pointeur [**D3DXMATRIX**](d3dxmatrix.md) retourné par cette méthode soit valide après les opérations de pile suivantes.

Notez que cette méthode ne supprime pas la matrice actuelle du haut de la pile ; au lieu de cela, elle retourne simplement la matrice actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack ::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack ::P par émission**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




