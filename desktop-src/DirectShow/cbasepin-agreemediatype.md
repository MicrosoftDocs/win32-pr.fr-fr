---
description: La méthode AgreeMediaType recherche un type de média pour établir une connexion de code confidentiel.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Méthode CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533463"
---
# <a name="cbasepinagreemediatype-method"></a>Méthode CBasePin. AgreeMediaType

La `AgreeMediaType` méthode recherche un type de média pour établir une connexion de code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT AgreeMediaType(
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

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie un type de média, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Opération réussie.<br/>                            |
| <dl> <dt>**VFW \_ E \_ aucun \_ \_ type acceptable**</dt> </dl> | Aucun type de média acceptable n’a été trouvé.<br/> |



 

## <a name="remarks"></a>Notes

Si le paramètre *VPM* est non **null** et qu’il spécifie complètement un type de média, cette méthode tente une connexion à l’aide de ce type de média. Si la tentative échoue, la méthode retourne une erreur.

Si le paramètre *VPM* a la **valeur null** ou qu’il spécifie un type de média partiel, cette méthode essaie les types de média dans l’ordre suivant :

1.  Types de médias préférés du pin de réception.
2.  Types de média préférés de ce pin.

Les types de média préférés sont énumérés avec la méthode [**CBasePin :: EnumMediaTypes**](cbasepin-enummediatypes.md) , et l’énumérateur résultant est passé à la méthode [**CBasePin :: TryMediaTypes**](cbasepin-trymediatypes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




