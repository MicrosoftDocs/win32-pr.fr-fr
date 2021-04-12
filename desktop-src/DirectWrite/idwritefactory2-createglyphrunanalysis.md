---
title: Méthode IDWriteFactory2 CreateGlyphRunAnalysis
description: Crée un objet d’analyse de série de glyphes, qui encapsule les informations utilisées pour restituer une exécution de glyphe.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Écriture directe de la méthode CreateGlyphRunAnalysis
- Méthode CreateGlyphRunAnalysis Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384927"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>IDWriteFactory2 :: CreateGlyphRunAnalysis, méthode

Crée un objet d’analyse de série de glyphes, qui encapsule les informations utilisées pour restituer une exécution de glyphe.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GlyphRun* \[ dans\]
</dt> <dd>

Type : **const [**DWRITE \_ Glyphs \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _

Structure spécifiant les propriétés de l’exécution du glyphe.

</dd> <dt>

_transform * \[ in, facultatif\]
</dt> <dd>

Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Transformation facultative appliquée aux glyphes et à leurs positions. Cette transformation est appliquée après la mise à l’échelle spécifiée par emSize et pixelsPerDip.

</dd> <dt>

_renderingMode * 
</dt> <dd>

Type : **\_ \_ mode de rendu DWRITE**

Spécifie le mode de rendu, qui doit être l’un des modes de rendu raster (c.-à-d., pas par défaut ni plan).

</dd> <dt>

*measuringMode* 
</dt> <dd>

Type : **[ **\_ \_ mode de mesure DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Spécifie la méthode pour mesurer les glyphes.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Type : **[ **\_ \_ \_ mode ajuster à la grille DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Comment adapter les contours de glyphe. Il ne doit pas être défini par défaut.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Type : **[ **DWRITE \_ Text \_ anticrénelage \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Spécifie le mode d’anticrénelage.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Type : **float**

Position horizontale de l’origine de la ligne de base, en DIP.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Type : **float**

Position verticale de l’origine de la ligne de base, en DIP.

</dd> <dt>

*glyphRunAnalysis* \[ à\]
</dt> <dd>

Type : **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Reçoit un pointeur vers l’objet nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

