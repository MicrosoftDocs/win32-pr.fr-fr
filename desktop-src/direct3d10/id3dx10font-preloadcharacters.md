---
description: Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: ID3DX10Font ::P méthode reloadCharacters (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a6c0ac515457aee430dea7cc3f785ed2832aed5c566f84b9d4ee262ba8b5cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953569"
---
# <a name="id3dx10fontpreloadcharacters-method"></a>ID3DX10Font ::P méthode reloadCharacters

Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.

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

## <a name="remarks"></a>Remarques

Cette méthode génère des textures contenant des glyphes qui représentent les caractères d’entrée. Les glyphes sont dessinés sous la forme d’une série de triangles.

Les caractères ne sont pas rendus à l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer les caractères. Toutefois, en préchargeant les caractères dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.

Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).

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

 

 
