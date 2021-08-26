---
description: La méthode SetPalette installe une palette pour la fenêtre. Cette méthode n’a aucun paramètre.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Méthode CBaseWindow. SetPalette (Winutil. h)-aucun paramètre
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052149"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Méthode CBaseWindow. SetPalette (Winutil. h)-aucun paramètre

La `SetPalette` méthode installe une palette pour la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Un appel interne à **GdiFlush** a retourné une erreur.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                            |



 

## <a name="remarks"></a>Remarques

La palette indiquée par la variable membre [**CBaseWindow :: m \_ HPALETTE**](cbasewindow-m-hpalette.md) est sélectionnée. L’appelant doit garantir la validité de **m \_ HPALETTE**.

Si la valeur de la variable membre [**CBaseWindow :: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) est **false** (valeur par défaut), cette méthode sélectionne la palette et la réalise. Dans le cas contraire, il sélectionne la palette, mais ne le réalise pas. L’objet ne supprime pas les palettes précédentes qu’il utilisait. L’appelant est responsable de la suppression des palettes.

Tout thread peut appeler cette méthode en toute sécurité, pas seulement le thread qui possède la fenêtre. La fenêtre envoie un message privé à lui-même, ce qui déclenche un appel à la méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Winutil. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




