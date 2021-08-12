---
description: Ajoute une animation définie au contrôleur d’animation.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'ID3DXAnimationController :: RegisterAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c6572b4a09967f2a911ffb3b147f3786aae75d71650d4d77d0564c1dbefc5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296979"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a>ID3DXAnimationController :: RegisterAnimationSet, méthode

Ajoute une animation définie au contrôleur d’animation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAnimSet* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




