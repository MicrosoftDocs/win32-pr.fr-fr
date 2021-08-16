---
description: À partir de la liste des types de média, la méthode TryMediaTypes tente de terminer une connexion à l’aide de l’un de ces types.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Méthode CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108619"
---
# <a name="cbasepintrymediatypes-method"></a>Méthode CBasePin. TryMediaTypes

À partir d’une liste de types de média, la `TryMediaTypes` méthode tente de terminer une connexion à l’aide de l’un de ces types.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
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

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui limite les types de média possibles, ou **null**.

</dd> <dt>

*pEnum* 
</dt> <dd>

Pointeur vers une interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , utilisé pour énumérer la liste des types de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                  | Description                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                               |
| <dl> <dt>**VFW \_ E \_ aucun \_ \_ type acceptable**</dt> </dl> | Impossible de trouver un type de média acceptable.<br/> |



 

## <a name="remarks"></a>Remarques

Pour chaque type de média retourné par l’interface **IEnumMediaTypes** , cette méthode tente une connexion en appelant la méthode [**CBasePin :: AttemptConnection**](cbasepin-attemptconnection.md) .

Si le paramètre *VPM* est non **null**, le code PIN ignore les types de média qui ne correspondent pas à ce type. Le paramètre *VPM* peut spécifier un type de média partiel. Un type de média partiel a une valeur de GUID \_ null pour le type principal, le sous-type ou le format. La \_ valeur null GUID correspond à n’importe quel type, similaire à une valeur « caractère générique ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




