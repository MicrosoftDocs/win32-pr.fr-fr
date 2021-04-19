---
description: 'La méthode Activate crée la fenêtre de boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: CBasePropertyPage. Activate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525476"
---
# <a name="cbasepropertypageactivate-method"></a>CBasePropertyPage. Activate, méthode

La `Activate` méthode crée la fenêtre de boîte de dialogue. Cette méthode implémente la méthode **IPropertyPage :: Activate** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue.

</dd> <dt>

*prect* 
</dt> <dd>

Pointeur vers une structure **Rect** qui contient des informations de positionnement pour la boîte de dialogue.

</dd> <dt>

*fModal* 
</dt> <dd>

Valeur booléenne indiquant si le cadre de la boîte de dialogue est modal (**true**) ou non modal (**false**).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>  | Erreur inattendue.<br/>        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




