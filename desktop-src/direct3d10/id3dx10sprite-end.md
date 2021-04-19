---
description: 'Appelez-le après ID3DX10Sprite :: Flush. Si \_ \_ \_ l’état de l’enregistrement d3dx10 Sprite a été spécifié lors de l’appel de ID3DX10Sprite :: Begin, cette API restaure l’état de l’appareil sur la manière dont il se trouvait avant l’appel de ID3DX10Sprite :: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite :: end, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539930"
---
# <a name="id3dx10spriteend-method"></a>ID3DX10Sprite :: end, méthode

Appelez-le après ID3DX10Sprite :: Flush. Si \_ \_ \_ l’état de l’enregistrement d3dx10 Sprite a été spécifié lors de l’appel de ID3DX10Sprite :: Begin, cette API restaure l’état de l’appareil sur la manière dont il se trouvait avant l’appel de ID3DX10Sprite :: Begin.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

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

 

 




