---
description: La \_ méthode put BorderColor modifie la couleur de la bordure.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Méthode CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc696efd1500d7cb2b9d66efcd8a1ccaa2fa215c1dd0c03516313b3766ff5dad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635896"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>CBaseControlWindow. put \_ BorderColor, méthode

La `put_BorderColor` méthode modifie la couleur de la bordure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Couleur* 
</dt> <dd>

Nouvelle couleur de bordure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Une application peut établir un rectangle de destination dans lequel la vidéo doit être affichée. Ce rectangle est relatif à la zone cliente de la fenêtre. Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une bordure entourant la vidéo. Cette propriété affecte la couleur utilisée par la bordure. Bien que le paramètre soit spécifié en tant que type **long** , il s’agit en fait d’une valeur **COLORREF** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




