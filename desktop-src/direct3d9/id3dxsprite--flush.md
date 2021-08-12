---
description: 'Force tous les sprites regroupés par lot à être envoyés à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DXSprite :: Begin. La liste des sprites regroupés par lot est alors effacée.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite :: Flush, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766fbe41491fc6861ac3eaf366c3a858870c560139f1048d405184b580e72229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292691"
---
# <a name="id3dxspriteflush-method"></a>ID3DXSprite :: Flush, méthode

Force tous les sprites regroupés par lot à être envoyés à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à [**ID3DXSprite :: Begin**](id3dxsprite--begin.md). La liste des sprites regroupés par lot est alors effacée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

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
</dt> <dt>

[**ID3DXSprite :: fin**](id3dxsprite--end.md)
</dt> </dl>

 

 




