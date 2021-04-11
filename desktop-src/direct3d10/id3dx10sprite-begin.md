---
description: Préparez un appareil pour dessiner des sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite :: Begin, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211854"
---
# <a name="id3dx10spritebegin-method"></a>ID3DX10Sprite :: Begin, méthode

Préparez un appareil pour dessiner des sprites.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Indicateurs qui contrôlent la façon dont les sprites seront dessinés. Consultez [**\_ \_ indicateur Sprite d3dx10**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Chaque appel à Begin doit être mis en correspondance avec un appel à [**ID3DX10Sprite :: end**](id3dx10sprite-end.md).

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

 

 
