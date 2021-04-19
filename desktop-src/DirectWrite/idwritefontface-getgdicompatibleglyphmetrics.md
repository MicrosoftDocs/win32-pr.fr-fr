---
title: Méthode IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Obtient des métriques de glyphes dans les unités de conception de police avec les valeurs de retour compatibles avec ce que le GDI produirait.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Écriture directe de la méthode GetGdiCompatibleGlyphMetrics
- Méthode GetGdiCompatibleGlyphMetrics Write directe, interface IDWriteFontFace
- Écriture directe de l’interface IDWriteFontFace, méthode GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543235"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>IDWriteFontFace :: GetGdiCompatibleGlyphMetrics, méthode

Obtient des métriques de glyphes dans les unités de conception de police avec les valeurs de retour compatibles avec ce que le GDI produirait.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*emSize* 
</dt> <dd>

Type : **float**

Taille ogique de la police en unités DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Type : **float**

Nombre de pixels physiques par DIP.

</dd> <dt>

*transformation* \[ dans, facultatif\]
</dt> <dd>

Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Transformation facultative appliquée aux glyphes et à leurs positions. Cette transformation est appliquée après la mise à l’échelle spécifiée par la taille de police et *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Type : **bool**

Quand la valeur est **false**, les mesures sont les mêmes que celles du texte d’alias GDI. Quand la valeur est **true**, les métriques sont les mêmes que les métriques du texte mesurées par GDI à l’aide d’une police créée avec la **\_ \_ qualité naturelle CLEARTYPE**.

</dd> <dt>

*GlyphIndices* \[ dans\]
</dt> <dd>

Type : **const UINT16 \***

Tableau d’index de glyphes pour lequel calculer les métriques.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Type : **UInt32**

Nombre d’éléments dans le tableau *GlyphIndices* .

</dd> <dt>

*glyphMetrics* \[ à\]
</dt> <dd>

Type : **[ **\_ \_ métriques de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Tableau de structures [**de \_ \_ métriques de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) remplies par cette fonction. Les métriques sont des unités de conception de police.

</dd> <dt>

*isSideways* 
</dt> <dd>

Type : **bool**

Valeur BOOLÉENNE qui indique si la police est utilisée dans une exécution latérale. Cela peut affecter les métriques de glyphe si la police a une simulation oblique, car la simulation oblique latérale diffère de la simulation oblique non latérale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Code d’erreur **HRESULT** standard. Si l’un des index de glyphes d’entrée se trouve en dehors de la plage d’index de glyphes valide pour le type de police actuel, **E \_ INVALIDARG** sera retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

