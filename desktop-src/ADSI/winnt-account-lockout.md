---
title: Verrouillage de compte (fournisseur WinNT)
description: Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant le nombre de minutes spécifié par l’attribut lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Verrouillage de compte ADSI, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, verrouillage de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e28c2a4bf58f5559070af78ca55235e8b10c16b2b856a63a256767d4d67a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838359"
---
# <a name="account-lockout-winnt-provider"></a>Verrouillage de compte (fournisseur WinNT)

Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant le nombre de minutes spécifié par l’attribut [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . La propriété [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) semble être la propriété à utiliser pour lire et modifier l’état de verrouillage d’un compte d’utilisateur, mais le fournisseur ADSI Winnt a des restrictions qui limitent l’utilisation de la propriété **IsAccountLocked** .

## <a name="resetting-the-account-lockout-status"></a>Réinitialisation de l’état de verrouillage de compte

Lorsque vous utilisez le fournisseur WinNT, la propriété [**IsAccountLocked**](iadsuser-property-methods.md) peut uniquement avoir la valeur **false**, ce qui déverrouille le compte. Toute tentative d’affecter la valeur **true** à la propriété **IsAccountLocked** échouera. Seul le système peut verrouiller un compte.

l’exemple de code suivant montre comment utiliser Visual Basic avec ADSI pour déverrouiller un compte d’utilisateur.


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



L’exemple de code suivant montre comment utiliser C++ avec ADSI pour déverrouiller un compte d’utilisateur.


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>Lecture de l’état de verrouillage de compte

Avec le fournisseur WinNT, la propriété [**IsAccountLocked**](iadsuser-property-methods.md) peut être utilisée pour déterminer si un compte est verrouillé. Si un compte est verrouillé, la propriété **IsAccountLocked** contient la **valeur true**. Si un compte n’est pas verrouillé, la propriété **IsAccountLocked** contient la **valeur false**.

l’exemple de code suivant montre comment utiliser Visual Basic avec ADSI pour déterminer si un compte est verrouillé.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



L’exemple de code suivant montre comment utiliser C++ avec ADSI pour déterminer si un compte est verrouillé.


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 