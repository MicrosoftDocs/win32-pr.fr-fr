---
description: 'Forcer l’envoi de tous les sprites par lot à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DX10Sprite :: Begin. La liste des sprites regroupés par lot est alors effacée.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite :: Flush, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915563"
---
# <a name="id3dx10spriteflush-method"></a>ID3DX10Sprite :: Flush, méthode

Forcer l’envoi de tous les sprites par lot à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DX10Sprite :: Begin. La liste des sprites regroupés par lot est alors effacée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Spécifications



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

 

 




