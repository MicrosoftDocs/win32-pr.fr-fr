---
description: 'La méthode GetPageInfo récupère des informations sur la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Méthode CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537793"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>Méthode CBasePropertyPage. GetPageInfo

La `GetPageInfo` méthode récupère des informations sur la page de propriétés. Cette méthode implémente la méthode **IPropertyPage :: GetPageInfo** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Pointeur vers une structure **PROPPAGEINFO** allouée par l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                   | Description                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




