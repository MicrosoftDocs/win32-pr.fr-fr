---
description: La méthode DoRealisePalette réalise la palette actuelle de la fenêtre.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Méthode CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530413"
---
# <a name="cbasewindowdorealisepalette-method"></a>Méthode CBaseWindow. DoRealisePalette

La `DoRealisePalette` méthode réalise la palette actuelle de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bForceBackground* 
</dt> <dd>

Valeur booléenne qui spécifie si la palette est forcée à être une palette d’arrière-plan. Pour plus d’informations, consultez **SelectPalette** dans le kit de développement Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Un appel interne à **GdiFlush** a retourné une erreur.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                            |



 

## <a name="remarks"></a>Notes

La méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) appelle cette méthode. Pour définir une nouvelle palette, appelez la méthode [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




