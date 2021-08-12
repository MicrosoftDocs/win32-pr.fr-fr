---
description: Dessinez du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font ::D méthode rawText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303169"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font ::D méthode rawText

Dessinez du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.

## <a name="syntax"></a>Syntaxe


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSprite* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Pointeur vers un objet ID3DX10Sprite qui contient la chaîne que vous souhaitez dessiner. Peut avoir la **valeur null**, auquel cas Direct3D affiche la chaîne avec son propre objet Sprite. Pour améliorer l’efficacité, un objet Sprite doit être spécifié si ID3DX10Font ::D rawText doit être appelé plusieurs fois dans une ligne.

</dd> <dt>

*pString* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne à dessiner. Si UNICODE est défini, ce type de paramètre correspond à un LPCWSTR, dans le cas contraire, le type correspond à un LPCSTR. Si le paramètre count a la valeur-1, la chaîne doit se terminer par **null** .

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

Nombre de caractères dans la chaîne. Si Count a la valeur-1, le paramètre pString est supposé être un pointeur vers un sprite contenant une chaîne se terminant par un caractère NULL et ID3DX10Font ::D rawText calcule le nombre de caractères automatiquement.

</dd> <dt>

*pRect* \[ dans\]
</dt> <dd>

Type : **LPRECT**

Pointeur vers une structure [Rect](/previous-versions//ms536136(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme. Comme avec n’importe quel objet RECT, la valeur de coordonnée du côté droit du rectangle doit être supérieure à celle de son côté gauche. De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Spécifiez la méthode de mise en forme du texte. Il peut s’agir de n’importe quelle combinaison des valeurs suivantes :



| Élément                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT en \_ bas<br/>             | Justifie le texte en bas du rectangle. Cette valeur doit être combinée avec DT \_ Singleline.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>\_CALCRECT DT<br/>       | Indiquez à DrawText de calculer automatiquement la largeur et la hauteur du rectangle en fonction de la longueur de la chaîne que vous lui indiquez de dessiner. S’il y a plusieurs lignes de texte, ID3DX10Font ::D rawText utilise la largeur du rectangle vers lequel pointe le paramètre pRect et étend la base du rectangle pour délimiter la dernière ligne de texte. S’il n’existe qu’une seule ligne de texte, ID3DX10Font ::D rawText modifie le côté droit du rectangle afin qu’il limite le dernier caractère de la ligne. Dans les deux cas, ID3DX10Font ::D rawText retourne la hauteur du texte mis en forme, mais ne dessine pas le texte.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>\_Centre DT<br/>             | Centrer le texte horizontalement dans le rectangle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>\_ExpandTabs DT<br/> | Développez caractères de tabulation. Le nombre par défaut de caractères par tabulation est huit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT à \_ gauche<br/>                   | Aligner le texte à gauche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip<br/>             | Dessin sans découpage. ID3DX10Font ::D rawText est un peu plus rapide lorsque DT \_ noclip est utilisé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT- \_ droit<br/>                | Aligner le texte à droite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>\_RTLREADING DT<br/> | Affichez le texte dans l’ordre de lecture de droite à gauche pour le texte bidirectionnel lorsqu’une police hébraïque ou arabe est sélectionnée. L’ordre de lecture par défaut pour tout le texte est de gauche à droite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ Singleline<br/> | Affichez le texte sur une seule ligne. Les retours chariot et les sauts de ligne n’interrompent pas la ligne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT en \_ haut<br/>                      | Texte de justification en haut.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_VCENTER DT<br/>          | Centrer le texte verticalement (une seule ligne).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>\_WordBreak DT<br/>    | Mots insécables. Les lignes sont automatiquement réparties entre les mots si un mot s’étend au-delà du bord du rectangle spécifié par le paramètre pRect. Une séquence de retour chariot/saut de ligne interrompt également la ligne.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Couleur du texte. Consultez [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **int**](../winprog/windows-data-types.md)**

Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques. Si DT \_ VCENTER ou DT \_ Bottom est spécifié, la valeur de retour est le décalage de pRect (de haut en bas) du texte dessiné. Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

Les paramètres de cette méthode sont très similaires à ceux de la fonction [GDI DrawText](/previous-versions//ms533909(v=vs.85)) .

Cette méthode prend en charge les chaînes ANSI et Unicode.

À moins que le \_ format DT NOclip ne soit utilisé, cette méthode découpe le texte afin qu’il n’apparaisse pas en dehors du rectangle spécifié. Toute la mise en forme est supposée avoir plusieurs lignes, sauf si le \_ format DT Singleline est spécifié.

Si la police sélectionnée est trop grande pour le rectangle, cette méthode n’essaie pas de remplacer une police plus petite.

Cette méthode prend en charge uniquement les polices dont l’échappement et l’orientation sont toutes deux égales à zéro.

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

 

 
