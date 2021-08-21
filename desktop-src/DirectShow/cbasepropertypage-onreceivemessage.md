---
description: La méthode OnReceiveMessage est appelée lorsque la boîte de dialogue reçoit un message.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Méthode CBasePropertyPage. OnReceiveMessage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833f0f7ab9192d88440afff75a36fee744ac2fe053c6fe99d1940686c452799a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158131"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>Méthode CBasePropertyPage. OnReceiveMessage

La `OnReceiveMessage` méthode est appelée lorsque la boîte de dialogue reçoit un message.

## <a name="syntax"></a>Syntaxe


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle vers la fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

Premier paramètre de message.

</dd> <dt>

*lParam* 
</dt> <dd>

Deuxième paramètre de message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur booléenne. La procédure de dialogue retourne cette valeur ; Pour plus d’informations, consultez la documentation du kit de développement Platform SDK.

## <a name="remarks"></a>Remarques

L’implémentation de la classe de base appelle **DefWindowProc**. Substituez cette méthode pour gérer les messages liés aux contrôles de boîte de dialogue. Si la méthode de substitution ne gère pas un message particulier, elle doit appeler la méthode de la classe de base.

Si l’utilisateur modifie des propriétés via les contrôles de boîte de dialogue, affectez la valeur **true** à l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) . Appelez ensuite la méthode **IPropertyPageSite :: OnStatusChange** sur le pointeur [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) pour informer le frame.

## <a name="examples"></a>Exemples

L’exemple suivant répond à un clic sur un bouton en mettant à jour une variable membre, qui est supposée être définie dans la classe dérivée. Cet exemple montre également une fonction d’assistance pour définir l’état d’intégrité de la page de propriétés.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
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

 

 




