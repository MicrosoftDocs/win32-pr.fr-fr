---
description: L’interface ID3DX10Font encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interface ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540345"
---
# <a name="id3dx10font-interface"></a>Interface ID3DX10Font

L’interface ID3DX10Font encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.

## <a name="members"></a>Membres

L’interface **ID3DX10Font** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Font** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10Font** possède ces méthodes.



| Méthode                                                     | Description                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dx10font-drawtext.md)                   | Dessinez du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Retourne un handle vers un contexte de périphérique (DC) d’affichage sur lequel la police est définie.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Obtient une description de l’objet de police en cours.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Récupérez l’appareil Direct3D associé à l’objet font.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Récupérez les caractéristiques de police.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Chargez une série de caractères dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | Chargez une série de glyphes dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.<br/> |



 

## <a name="remarks"></a>Remarques

L’interface ID3DX10Font est obtenue en appelant [**D3DX10CreateFont**](d3dx10createfont.md) ou [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).

Le type LPD3DX10FONT est défini comme un pointeur vers l’interface ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
