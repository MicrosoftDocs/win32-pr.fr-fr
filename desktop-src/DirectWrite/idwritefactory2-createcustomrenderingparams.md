---
title: Méthode IDWriteFactory2 CreateCustomRenderingParams
description: Crée un objet de paramètres de rendu avec les propriétés spécifiées.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Écriture directe de la méthode CreateCustomRenderingParams
- Méthode CreateCustomRenderingParams Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384928"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>IDWriteFactory2 :: CreateCustomRenderingParams, méthode

Crée un objet de paramètres de rendu avec les propriétés spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*gamma* 
</dt> <dd>

Type : **float**

Valeur gamma utilisée pour la correction gamma, qui doit être supérieure à zéro et ne peut pas dépasser 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Type : **float**

La quantité d’amélioration du contraste, zéro ou une valeur supérieure.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Type : **float**

La quantité d’amélioration du contraste, zéro ou une valeur supérieure.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Type : **float**

Degré de niveau ClearType, de 0.0 f (no ClearType) à 1.0 f (Full ClearType).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Type : **[ **DWRITE \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Géométrie d’un pixel d’appareil.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Type : **[ **\_ \_ mode de rendu DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Méthode de rendu des glyphes. Dans la plupart des cas, il doit s’agir du \_ mode de rendu DWRITE \_ \_ par défaut pour utiliser automatiquement un mode approprié.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Type : **[ **\_ \_ \_ mode ajuster à la grille DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Comment ajuster les contours de glyphes. Dans la plupart des cas, il doit s’agir de la \_ grille DWRITE \_ \_ par défaut pour choisir automatiquement un mode approprié.

</dd> <dt>

*renderingParams* \[ à\]
</dt> <dd>

Type : **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Contient l’objet de paramètres de rendu nouvellement créé, ou NULL en cas d’échec.

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

 

