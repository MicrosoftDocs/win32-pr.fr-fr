---
title: Expiration du compte (fournisseur LDAP)
description: Pour définir la date d’expiration du compte, affectez à la propriété IADsUser. AccountExpirationDate la valeur de date souhaitée.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- ADSI d’expiration de compte, fournisseur LDAP
- ADSI Provider ADSI, exemples de gestion des utilisateurs, expiration du compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510707"
---
# <a name="account-expiration-ldap-provider"></a>Expiration du compte (fournisseur LDAP)

Pour définir la date d’expiration du compte, affectez à la propriété [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) la valeur de date souhaitée. Pour désactiver la date d’expiration du compte, affectez la valeur zéro à l’attribut [**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires) . Les exemples de code suivants montrent comment définir la date d’expiration.


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> L’attribut [**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires) contient la date d’expiration du compte. Le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory affiche la date à laquelle le compte expirera à la fin de. Autrement dit, le composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs affiche la date d’expiration du compte à un jour antérieur à la date contenue dans l’attribut **AccountExpires dans** .

 

 

 