---
description: 'La méthode ConnectionMediaType récupère le type de média pour la connexion de code confidentiel actuelle, le cas échéant. Cette méthode implémente la méthode IPin :: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Méthode CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdeed52a212a659ca280163ea9513f0cb4f373ea2686bfde00078ebccb183daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916749"
---
# <a name="cbasepinconnectionmediatype-method"></a>Méthode CBasePin. ConnectionMediaType

La méthode **ConnectionMediaType** récupère le type de média pour la connexion de code confidentiel actuelle, le cas échéant. Cette méthode implémente la méthode [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui reçoit le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/>      |



 

## <a name="remarks"></a>Remarques

Si le code PIN est connecté, cette méthode copie le type de média dans la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) spécifiée par *VPM*. L’appelant doit libérer le bloc de format du type de média. Vous pouvez utiliser la fonction [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ou la fonction d’assistance [**FreeMediaType**](freemediatype.md) .

Si le code pin n’est pas connecté, cette méthode zéro le bloc de mémoire spécifié par *VPM* et retourne un code d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

