---
description: L’interface ID3DXFont encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interface ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998580"
---
# <a name="id3dxfont-interface"></a>Interface ID3DXFont

L’interface ID3DXFont encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.

## <a name="members"></a>Membres

L’interface **ID3DXFont** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFont** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFont** possède ces méthodes.



| Méthode                                                    | Description                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dxfont--drawtext.md)                   | Dessine du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Retourne un handle vers un contexte de périphérique (DC) d’affichage dont la police est définie.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Obtient une description de l’objet de police en cours. GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une structure [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ DESCA** , respectivement.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Récupère le périphérique Direct3D associé à l’objet font.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Récupère les caractéristiques de police qui sont identifiées dans une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Charge une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Charge une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.<br/>                                                                                        |



 

## <a name="remarks"></a>Notes

L’interface **ID3DXFont** est obtenue en appelant [**D3DXCreateFont**](d3dxcreatefont.md) ou [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).

Le type LPD3DXFONT est défini comme un pointeur vers l’interface **ID3DXFont** .


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
