---
description: La méthode Deactivate détruit la fenêtre de boîte de dialogue. Cette méthode implémente la méthode IPropertyPage ::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: CBasePropertyPage. Deactivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545535"
---
# <a name="cbasepropertypagedeactivate-method"></a>CBasePropertyPage. Deactivate, méthode

La `Deactivate` méthode détruit la fenêtre de boîte de dialogue. Cette méthode implémente la méthode **IPropertyPage ::D eactivate** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>            |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage :: OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




