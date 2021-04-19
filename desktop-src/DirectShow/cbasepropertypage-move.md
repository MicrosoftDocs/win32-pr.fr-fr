---
description: 'La méthode Move positionne et redimensionne la boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: CBasePropertyPage. Move, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526324"
---
# <a name="cbasepropertypagemove-method"></a>CBasePropertyPage. Move, méthode

La `Move` méthode positionne et redimensionne la boîte de dialogue. Cette méthode implémente la méthode **IPropertyPage :: Move** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*prect* 
</dt> <dd>

Pointeur vers une structure **Rect** contenant les informations de positionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/>        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




