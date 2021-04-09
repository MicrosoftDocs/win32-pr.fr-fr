---
title: L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur LDAP)
description: Pour forcer un utilisateur à modifier son mot de passe à la prochaine ouverture de session, définissez l’attribut pwdLastSet sur zéro (0). Pour supprimer cette exigence, affectez la valeur-1 à l’attribut pwdLastSet. L’attribut pwdLastSet ne peut pas être défini sur une autre valeur, sauf par le système.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- L’utilisateur doit changer de mot de passe à la prochaine ouverture de session ADSI, fournisseur LDAP
- ADSI Provider ADSI, exemples de gestion des utilisateurs, l’utilisateur doit changer de mot de passe à la prochaine ouverture de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028544"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur LDAP)

Pour forcer un utilisateur à modifier son mot de passe à la prochaine ouverture de session, définissez l’attribut **pwdLastSet** sur zéro (0). Pour supprimer cette exigence, affectez la valeur-1 à l’attribut **pwdLastSet** . L’attribut **pwdLastSet** ne peut pas être défini sur une autre valeur, sauf par le système.

L’exemple de code suivant montre comment définir l’option « l’utilisateur doit changer le mot de passe à la prochaine ouverture de session ».


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



L’exemple de code suivant montre comment définir l’option « l’utilisateur doit changer le mot de passe à la prochaine ouverture de session ».


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




