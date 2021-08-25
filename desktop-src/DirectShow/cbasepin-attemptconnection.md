---
description: La méthode AttemptConnection se connecte à un autre code confidentiel à l’aide d’un type de média spécifié.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Méthode CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e70683d5307b81db14d23fec2c163b085cccaf64b7926eb41efdb5dfe9ac7611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872393"
---
# <a name="cbasepinattemptconnection-method"></a>Méthode CBasePin. AttemptConnection

La `AttemptConnection` méthode se connecte à un autre code confidentiel à l’aide d’un type de média spécifié.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin de réception.

</dd> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                | Description                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                          |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Le type de média n’est pas acceptable.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode tente de connecter les deux broches avec un type de média spécifique. Si le type n’est pas acceptable, la méthode échoue sans essayer d’autres types de média.

Si le type de média est acceptable, cette méthode appelle la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) du pin de réception. Elle appelle ensuite la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) pour terminer la connexion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




