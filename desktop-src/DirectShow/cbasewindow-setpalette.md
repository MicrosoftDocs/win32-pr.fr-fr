---
description: La méthode SetPalette installe une palette pour la fenêtre.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Méthode CBaseWindow. SetPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543789"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Méthode CBaseWindow. SetPalette (Winutil. h)

La `SetPalette` méthode installe une palette pour la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPalette* 
</dt> <dd>

Handle vers la nouvelle palette. Ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Un appel interne à **GdiFlush** a retourné une erreur.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                            |



 

## <a name="remarks"></a>Notes

Si la valeur de la variable membre [**CBaseWindow :: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) est **false** (valeur par défaut), cette méthode sélectionne la palette et la réalise. Dans le cas contraire, il sélectionne la palette, mais ne le réalise pas. L’objet ne supprime pas les palettes précédentes qu’il utilisait. L’appelant est responsable de la suppression des palettes.

Tout thread peut appeler cette méthode en toute sécurité, pas seulement le thread qui possède la fenêtre. La fenêtre envoie un message privé à lui-même, ce qui déclenche un appel à la méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




