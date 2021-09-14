---
description: La méthode RefreshDisplayType met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Méthode CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119950"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>Méthode CImageDisplay. RefreshDisplayType

La `RefreshDisplayType` méthode met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szDeviceName* 
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** . Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou \_ si E échoue en cas d’échec.

## <a name="remarks"></a>Notes

Cette méthode initialise le membre **d' \_ affichage m** sur un type vidéo qui correspond au mode d’affichage sur le périphérique spécifié.

Appelez cette méthode chaque fois qu’un \_ message DISPLAYCHANGED WM est reçu, ou pour spécifier un périphérique d’affichage secondaire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageDisplay, classe**](cimagedisplay.md)
</dt> </dl>

 

 




