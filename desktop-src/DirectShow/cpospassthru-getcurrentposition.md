---
description: 'La méthode GetCurrentPosition récupère la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Méthode CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012272"
---
# <a name="cpospassthrugetcurrentposition-method"></a>Méthode CPosPassThru. GetCurrentPosition

La `GetCurrentPosition` méthode récupère la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | La méthode n’est pas prise en charge.<br/>   |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**CPosPassThru :: GetMediaTime**](cpospassthru-getmediatime.md) pour récupérer la position la plus récente. Si **GetMediaTime** échoue, la méthode appelle **IMediaSeeking :: getCurrentPosition** sur l’épingle connecté.

La méthode **GetMediaTime** échoue par défaut dans la classe de base. Si votre filtre met en cache la position actuelle, substituez **GetMediaTime** pour retourner la valeur mise en cache.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




