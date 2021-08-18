---
description: Dessine du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont ::D méthode rawText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987419"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont ::D méthode rawText

Dessine du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.

## <a name="syntax"></a>Syntaxe


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSprite* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Pointeur vers un objet [**ID3DXSprite**](id3dxsprite.md) qui contient la chaîne. Peut avoir la **valeur null**, auquel cas Direct3D affiche la chaîne avec son propre objet Sprite. Pour améliorer l’efficacité, un objet Sprite doit être spécifié si **DrawText** doit être appelé plusieurs fois dans une ligne.

</dd> <dt>

*pString* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne à dessiner. Si le paramètre count a la valeur-1, la chaîne doit se terminer par un caractère null.

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

Spécifie le nombre de caractères de la chaîne. Si Count a la valeur-1, le paramètre pString est supposé être un pointeur vers une chaîne terminée par le caractère null et **DrawText** calcule automatiquement le nombre de caractères.

</dd> <dt>

*pRect* \[ dans\]
</dt> <dd>

Type : **[ **LPRECT**](../winprog/windows-data-types.md)**

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme. La valeur de coordonnée du côté droit du rectangle doit être supérieure à celle du côté gauche. De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie la méthode de mise en forme du texte. Il peut s’agir de n’importe quelle combinaison des valeurs suivantes :



| Valeur                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT en \_ bas**</dt> </dl>             | Justifie le texte en bas du rectangle. Cette valeur doit être combinée avec DT \_ Singleline.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**\_CALCRECT DT**</dt> </dl>       | Détermine la largeur et la hauteur du rectangle. S’il y a plusieurs lignes de texte, **DrawText** utilise la largeur du rectangle vers lequel pointe le paramètre pRect et étend la base du rectangle pour délimiter la dernière ligne de texte. S’il n’existe qu’une seule ligne de texte, **DrawText** modifie le côté droit du rectangle afin qu’il limite le dernier caractère de la ligne. Dans les deux cas, **DrawText** retourne la hauteur du texte mis en forme, mais ne dessine pas le texte.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**\_Centre DT**</dt> </dl>             | Centre le texte horizontalement dans le rectangle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**\_ExpandTabs DT**</dt> </dl> | Développe des caractères de tabulation. Le nombre par défaut de caractères par tabulation est huit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT à \_ gauche**</dt> </dl>                   | Aligne le texte à gauche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOclip**</dt> </dl>             | Dessine sans découpage. **DrawText** est un peu plus rapide lorsque DT \_ noclip est utilisé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT- \_ droit**</dt> </dl>                | Aligne le texte à droite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**\_RTLREADING DT**</dt> </dl> | Affiche le texte dans l’ordre de lecture de droite à gauche pour le texte bidirectionnel lorsqu’une police hébraïque ou arabe est sélectionnée. L’ordre de lecture par défaut pour tout le texte est de gauche à droite.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ Singleline**</dt> </dl> | Affiche du texte sur une seule ligne. Les retours chariot et les sauts de ligne n’interrompent pas la ligne.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT en \_ haut**</dt> </dl>                      | Top-justifie le texte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**\_VCENTER DT**</dt> </dl>          | Centre le texte verticalement (une seule ligne).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**\_WordBreak DT**</dt> </dl>    | Arrête les mots. Les lignes sont automatiquement réparties entre les mots si un mot s’étend au-delà du bord du rectangle spécifié par le paramètre pRect. Une séquence de retour chariot/saut de ligne interrompt également la ligne.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Couleur du texte. Pour plus d’informations, consultez [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **int**](../winprog/windows-data-types.md)**

Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques. Si DT \_ VCENTER ou DT \_ Bottom est spécifié, la valeur de retour est le décalage de pRect (de haut en bas) du texte dessiné. Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

Les paramètres de cette méthode sont très similaires à ceux de la fonction GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) .

Cette méthode prend en charge les chaînes ANSI et Unicode.

Cette méthode doit être appelée à l’intérieur d’un [**BeginScene**](/windows/desktop/api) ... Bloc [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) . La seule exception est lorsqu’une application appelle **DrawText** avec DT \_ CALCRECT pour calculer la taille d’un bloc de texte donné.

À moins que le \_ format DT NOclip ne soit utilisé, cette méthode découpe le texte afin qu’il n’apparaisse pas en dehors du rectangle spécifié. Toute la mise en forme est supposée avoir plusieurs lignes, sauf si le \_ format DT Singleline est spécifié.

Si la police sélectionnée est trop grande pour le rectangle, cette méthode n’essaie pas de remplacer une police plus petite.

Cette méthode prend en charge uniquement les polices dont l’échappement et l’orientation sont toutes deux égales à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
