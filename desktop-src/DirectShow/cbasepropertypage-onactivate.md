---
description: La méthode OnActivate est appelée lorsque la page de propriétés est activée.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: CBasePropertyPage. OnActivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052569"
---
# <a name="cbasepropertypageonactivate-method"></a>CBasePropertyPage. OnActivate, méthode

La `OnActivate` méthode est appelée lorsque la page de propriétés est activée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

L’implémentation de la classe de base retourne S \_ OK.

## <a name="remarks"></a>Remarques

La méthode [**CBasePropertyPage :: Activate**](cbasepropertypage-activate.md) appelle la `OnActivate` méthode. Dans votre classe dérivée, substituez `OnActivate` pour initialiser la boîte de dialogue.

## <a name="examples"></a>Exemples

L’exemple suivant initialise un contrôle TrackBar. Cet exemple suppose que **m \_ pOwningFilter** est un pointeur vers une interface personnalisée sur le filtre associé à la page de propriétés. (Utilisez la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) pour initialiser ces pointeurs.)


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




