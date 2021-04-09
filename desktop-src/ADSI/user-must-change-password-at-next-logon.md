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
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a><span data-ttu-id="6fbcd-107">L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur LDAP)</span><span class="sxs-lookup"><span data-stu-id="6fbcd-107">User Must Change Password at Next Logon (LDAP Provider)</span></span>

<span data-ttu-id="6fbcd-108">Pour forcer un utilisateur à modifier son mot de passe à la prochaine ouverture de session, définissez l’attribut **pwdLastSet** sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="6fbcd-108">To force a user to change their password at next logon, set the **pwdLastSet** attribute to zero (0).</span></span> <span data-ttu-id="6fbcd-109">Pour supprimer cette exigence, affectez la valeur-1 à l’attribut **pwdLastSet** .</span><span class="sxs-lookup"><span data-stu-id="6fbcd-109">To remove this requirement, set the **pwdLastSet** attribute to -1.</span></span> <span data-ttu-id="6fbcd-110">L’attribut **pwdLastSet** ne peut pas être défini sur une autre valeur, sauf par le système.</span><span class="sxs-lookup"><span data-stu-id="6fbcd-110">The **pwdLastSet** attribute cannot be set to any other value except by the system.</span></span>

<span data-ttu-id="6fbcd-111">L’exemple de code suivant montre comment définir l’option « l’utilisateur doit changer le mot de passe à la prochaine ouverture de session ».</span><span class="sxs-lookup"><span data-stu-id="6fbcd-111">The following code example shows how to set the "User must change password at next logon" option.</span></span>


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



<span data-ttu-id="6fbcd-112">L’exemple de code suivant montre comment définir l’option « l’utilisateur doit changer le mot de passe à la prochaine ouverture de session ».</span><span class="sxs-lookup"><span data-stu-id="6fbcd-112">The following code example shows how to set the "User must change password at next logon" option.</span></span>


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



 

 




