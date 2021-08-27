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
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108519"
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
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>  | Erreur inattendue.<br/>        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




