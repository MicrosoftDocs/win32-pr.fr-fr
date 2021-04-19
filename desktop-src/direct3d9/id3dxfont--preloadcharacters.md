---
description: Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: ID3DXFont ::P méthode reloadCharacters (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527954"
---
# <a name="id3dxfontpreloadcharacters-method"></a>ID3DXFont ::P méthode reloadCharacters

Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Premier* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

ID du premier caractère à charger dans la mémoire vidéo.

</dd> <dt>

*Dernière* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

ID du dernier caractère à charger dans la mémoire vidéo.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Cette méthode génère des textures contenant des glyphes qui représentent les caractères d’entrée. Les glyphes sont dessinés sous la forme d’une série de triangles.

Les caractères ne sont pas rendus à l’appareil ; [**DrawText**](id3dxfont--drawtext.md) doit toujours être appelé pour restituer les caractères. Toutefois, en préchargeant les caractères dans la mémoire vidéo, **DrawText** utilise beaucoup moins de ressources processeur.

Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
