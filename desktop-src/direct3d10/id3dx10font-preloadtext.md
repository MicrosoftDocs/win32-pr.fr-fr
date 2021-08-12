---
description: Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font ::P méthode reloadText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 23c7a3a8ce8ed3534a7369f167ce1045d200cbaeea1aa80653e05412ffa978e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302844"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font ::P méthode reloadText

Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pString* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne de caractères à charger dans la mémoire vidéo. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR ; dans le cas contraire, le type de données est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

Nombre de caractères dans la chaîne de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en PreloadTextW. Dans le cas contraire, l’appel de fonction est résolu en PreloadTextA, car les chaînes ANSI sont utilisées.

Cette méthode génère des textures qui contiennent des glyphes qui représentent le texte d’entrée. Les glyphes sont dessinés sous la forme d’une série de triangles.

Le texte ne sera pas rendu sur l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer le texte. Toutefois, en préchargeant du texte dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.

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

 

 
