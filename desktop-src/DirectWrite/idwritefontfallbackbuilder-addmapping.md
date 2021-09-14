---
title: Méthode IDWriteFontFallbackBuilder AddMapping
description: Ajoute un mappage unique à la liste. Appelez cette fois pour chaque mappage supplémentaire.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Écriture directe de la méthode AddMapping
- Méthode AddMapping Write directe, interface IDWriteFontFallbackBuilder
- Écriture directe de l’interface IDWriteFontFallbackBuilder, méthode AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123701"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>IDWriteFontFallbackBuilder :: AddMapping, méthode

Ajoute un mappage unique à la liste. Appelez cette fois pour chaque mappage supplémentaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*gamme* 
</dt> <dd>

Type : **[ **DWRITE \_ Unicode \_ Range**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Plages Unicode qui s’appliquent à ce mappage.

</dd> <dt>

*rangesCount* 
</dt> <dd>

Type : **UInt32**

Nombre de plages Unicode.

</dd> <dt>

*targetFamilyNames* \[ dans\]
</dt> <dd>

Type : **const WCHAR \* \***

Liste des chaînes du nom de la famille cible.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Type : **UInt32**

Nombre de noms de familles cibles.

</dd> <dt>

*fontCollection* \[ dans, facultatif\]
</dt> <dd>

Type : **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Collection de polices explicites facultative pour ce mappage.

</dd> <dt>

*localeName* \[ dans, facultatif\]
</dt> <dd>

Type : **const WCHAR \***

Paramètres régionaux du contexte.

</dd> <dt>

*baseFamilyName* \[ dans, facultatif\]
</dt> <dd>

Type : **const WCHAR \***

Nom de famille de base avec lequel effectuer la correspondance, le cas échéant.

</dd> <dt>

*scale* 
</dt> <dd>

Type : **float**

Facteur d’échelle pour multiplier la police de la cible du résultat par.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

