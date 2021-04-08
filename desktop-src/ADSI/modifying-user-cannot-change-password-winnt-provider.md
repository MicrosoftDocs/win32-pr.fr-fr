---
title: La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)
description: La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)
- L’utilisateur ne peut pas changer de mot de passe (fournisseur WinNT), modification
- ADSI Provider ADSI, exemples de gestion des utilisateurs, utilisateur ne peut pas modifier le mot de passe, modifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14e9bac51bae2edf4b9f6f571f20c75563a4d03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671134"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="d8f68-106">La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="d8f68-106">Modifying User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="d8f68-107">La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="d8f68-107">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="d8f68-108">Pour refuser cette autorisation, ajoutez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur à la propriété **userFlags** de l’objet User.</span><span class="sxs-lookup"><span data-stu-id="d8f68-108">To deny this permission, add the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag to the **userFlags** property of the user object.</span></span> <span data-ttu-id="d8f68-109">Pour accorder cette autorisation, supprimez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur de la propriété **userFlags** de l’objet User.</span><span class="sxs-lookup"><span data-stu-id="d8f68-109">To grant this permission, remove the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag from the **userFlags** property of the user object.</span></span>

## <a name="example-code"></a><span data-ttu-id="d8f68-110">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="d8f68-110">Example Code</span></span>

<span data-ttu-id="d8f68-111">L’exemple de code suivant montre comment modifier l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8f68-111">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



<span data-ttu-id="d8f68-112">L’exemple de code suivant montre comment modifier l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8f68-112">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




