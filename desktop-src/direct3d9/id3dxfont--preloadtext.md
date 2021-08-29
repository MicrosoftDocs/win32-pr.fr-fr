---
description: Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: ID3DXFont ::P méthode reloadText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 874b2d6106a7dcbfb8992a8677a28841f7d44e8b1512c6258b7e3bef45770eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629869"
---
# <a name="id3dxfontpreloadtext-method"></a>ID3DXFont ::P méthode reloadText

Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pString* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)\***

Pointeur vers une chaîne de caractères à charger dans la mémoire vidéo. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR ; dans le cas contraire, le type de données est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

Nombre de caractères dans la chaîne de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en PreloadTextW. Dans le cas contraire, l’appel de fonction est résolu en PreloadTextA, car les chaînes ANSI sont utilisées.

Cette méthode génère des textures qui contiennent des glyphes qui représentent le texte d’entrée. Les glyphes sont dessinés sous la forme d’une série de triangles.

Le texte ne sera pas rendu sur l’appareil ; [**DrawText**](id3dxfont--drawtext.md) doit encore être appelé pour restituer le texte. Toutefois, en préchargeant le texte dans la mémoire vidéo, **DrawText** utilise beaucoup moins de ressources processeur.

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

 

 
