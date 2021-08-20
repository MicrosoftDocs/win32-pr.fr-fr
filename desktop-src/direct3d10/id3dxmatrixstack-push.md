---
description: ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)-ajoute une matrice à la pile.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8c9054274666b41e70fa060d10a28309be929a19ee5c363ff4afeb76b25e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914235"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a>ID3DXMATRIXStack ::P méthode par émission (D3DX10. h)

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

## <a name="requirements"></a>Conditions requises



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

 

 




