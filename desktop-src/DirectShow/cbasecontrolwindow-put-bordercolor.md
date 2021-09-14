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
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094845"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Une application peut établir un rectangle de destination dans lequel la vidéo doit être affichée. Ce rectangle est relatif à la zone cliente de la fenêtre. Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une bordure entourant la vidéo. Cette propriété affecte la couleur utilisée par la bordure. Bien que le paramètre soit spécifié en tant que type **long** , il s’agit en fait d’une valeur **COLORREF** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




