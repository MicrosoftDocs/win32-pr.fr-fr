---
title: Méthode IDWriteFontFace GetGdiCompatibleMetrics
description: Obtient les unités de conception et les métriques communes pour le type de police. Ces métriques sont applicables à tous les glyphes d’un fontface et sont utilisées par les applications pour les calculs de disposition.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Écriture directe de la méthode GetGdiCompatibleMetrics
- Méthode GetGdiCompatibleMetrics Write directe, interface IDWriteFontFace
- Écriture directe de l’interface IDWriteFontFace, méthode GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525179"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>IDWriteFontFace :: GetGdiCompatibleMetrics, méthode

Obtient les unités de conception et les métriques communes pour le type de police. Ces métriques sont applicables à tous les glyphes d’un fontface et sont utilisées par les applications pour les calculs de disposition.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*emSize* 
</dt> <dd>

Type : **float**

Taille logique de la police en unités DIP.

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

*fontFaceMetrics* \[ à\]
</dt> <dd>

Type : **[ **\_ \_ métriques de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Pointeur vers une structure [**de \_ \_ mesure de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)à remplir. Les métriques retournées par cette fonction se trouvent dans les unités de conception de police.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Code d’erreur HRESULT standard.

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

 

