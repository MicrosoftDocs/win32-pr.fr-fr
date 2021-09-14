---
description: 'La méthode CBaseInputPin commence une opération de vidage. Cette méthode implémente la méthode IPin :: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Méthode CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123789"
---
# <a name="cbaseinputpinbeginflush-method"></a>Méthode CBaseInputPin. BeginFlush

La `CBaseInputPin` méthode commence une opération de vidage. Cette méthode implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode affecte à l’indicateur [**CBaseInputPin :: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) la **valeur true**, ce qui amène la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) à rejeter tout autre échantillon.

La classe dérivée doit substituer cette méthode et effectuer les étapes suivantes :

1.  Appelez la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur les broches d’entrée en aval. Si le pin n’a pas encore remis d’exemples de supports en aval, vous pouvez ignorer cette étape. Si vos broches de sortie dérivent de la classe [**CBaseOutputPin**](cbaseoutputpin.md) , vous pouvez appeler la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .
2.  Appelez la méthode de la classe de base.
3.  Début de la suppression des données en file d’attente.
4.  Retour de tous les appels bloqués à la méthode **Receive** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




