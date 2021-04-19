---
description: 'La méthode suivante récupère un nombre spécifié de types de médias. Cette méthode implémente la méthode IEnumMediaTypes :: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Méthode CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530976"
---
# <a name="cenummediatypesnext-method"></a>CEnumMediaTypes. Next, méthode

La `Next` méthode récupère un nombre spécifié de types de médias. Cette méthode implémente la méthode [**IEnumMediaTypes :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Nombre de types de médias à récupérer.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Tableau de pointeurs vers des structures de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de taille *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de types de médias que la méthode a retournés. Peut avoir la **valeur null** si *cMediaTypes* est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | N’a pas récupéré autant de types de média que nécessaire.<br/>                       |
| <dl> <dt>**\_OK**</dt> </dl>                       | Opération réussie.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argument non valide.<br/>                                                        |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                                               |
| <dl> <dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt> </dl> | L’état du pin a changé et est désormais incohérent avec l’énumérateur.<br/> |



 

## <a name="remarks"></a>Notes

Si la méthode est réussie, le tableau spécifié par *ppMediaTypes* contient des pointeurs vers des \_ structures de type de média am \_ . Le nombre de structures est égal à *\* pcFetched*. Libérez chaque type de média en appelant la fonction [**DeleteMediaType**](deletemediatype.md) .

Cette méthode appelle la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) du pin pour récupérer les types de média.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumMediaTypes, classe**](cenummediatypes.md)
</dt> </dl>

 

 




