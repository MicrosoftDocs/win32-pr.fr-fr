---
description: ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)-ajoute une matrice à la pile.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1211469b3b7cf90e9ddae1fd8edb51bb38d35b427f6cdf62684aa84142a77009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563939"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a>ID3DXMATRIXStack ::P méthode par émission (D3dx9math. h)

Ajoute une matrice à la pile.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Push();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode incrémente le nombre d’éléments sur la pile de 1, en dupliquant la matrice actuelle. La pile croît de manière dynamique à mesure que d’autres éléments sont ajoutés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack :: GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack ::P op**](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




