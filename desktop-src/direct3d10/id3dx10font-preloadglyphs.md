---
description: Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font ::P méthode reloadGlyphs (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540335"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font ::P méthode reloadGlyphs

Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Premier* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

ID du premier glyphe à charger dans la mémoire vidéo.

</dd> <dt>

*Dernière* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

ID du dernier glyphe à charger dans la mémoire vidéo.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Cette méthode génère des textures qui contiennent les glyphes d’entrée. Les glyphes sont dessinés sous la forme d’une série de triangles.

Les glyphes ne seront pas rendus à l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer les glyphes. Toutefois, en préchargeant les glyphes dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
