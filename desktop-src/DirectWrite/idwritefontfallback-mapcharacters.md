---
title: Méthode IDWriteFontFallback MapCharacters
description: Détermine une police appropriée à utiliser pour restituer la plage de texte de début.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Écriture directe de la méthode MapCharacters
- Méthode MapCharacters Write directe, interface IDWriteFontFallback
- Écriture directe de l’interface IDWriteFontFallback, méthode MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317310"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>IDWriteFontFallback :: MapCharacters, méthode

Détermine une police appropriée à utiliser pour restituer la plage de texte de début.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*source* 
</dt> <dd>

Tapez : **[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

L’implémentation de la source de texte contient le texte et les paramètres régionaux.

</dd> <dt>

_textPosition * 
</dt> <dd>

Type : **UInt32**

Position de départ à analyser.

</dd> <dt>

*textLength* 
</dt> <dd>

Type : **UInt32**

Longueur du texte à analyser.

</dd> <dt>

*baseFontCollection* \[ dans, facultatif\]
</dt> <dd>

Tapez : **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Collection de polices par défaut à utiliser.

</dd> <dt>

_baseFamilyName * \[ in, facultatif\]
</dt> <dd>

Type : **const WCHAR \_ t \** _

Nom de famille de la police de base. Si vous transmettez la valeur null, aucune correspondance n’est effectuée par rapport à la famille.

</dd> <dt>

_baseWeight * 
</dt> <dd>

Type : épaisseur de la **[ **\_ police \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Poids souhaité.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Type : **[ **DWRITE \_ \_ style de police**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Style souhaité.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Type : **[ **\_ \_ étirement de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Étirement souhaité.

</dd> <dt>

*mappedLength* \[ à\]
</dt> <dd>

Type : **UInt32 \** _

Longueur du texte mappé à la police mappée. Cela sera toujours inférieur ou égal à la longueur du texte et supérieur à zéro (si la longueur du texte est différente de zéro), de sorte que l’appelant avance au moins un caractère.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Type : **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Police qui doit être utilisée pour afficher les premiers caractères *mappedLength* du texte. Si elle retourne NULL, cela signifie qu’aucune police ne peut restituer le texte, et *mappedLength* est le nombre de caractères à ignorer (rendu avec un glyphe manquant).

</dd> <dt>

mise à l' *échelle* \[ à\]
</dt> <dd>

Type : **float \** _

Facteur d’échelle pour multiplier la taille em de la police retournée par.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                 |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

