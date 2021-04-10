---
title: La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur WinNT)
description: La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- La lecture de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT) ADSI
- L’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT) ADSI, lecture
- ADSI Provider ADSI, exemples de gestion des utilisateurs, utilisateur ne peut pas modifier le mot de passe, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab257f620d3e103866639f8ecacb57cc924efec4
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2020
ms.locfileid: "103940727"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="10ca7-106">La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="10ca7-106">Reading User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="10ca7-107">La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée.</span><span class="sxs-lookup"><span data-stu-id="10ca7-107">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="10ca7-108">Pour déterminer si cette autorisation a été accordée à l’utilisateur avec le fournisseur WinNT, lisez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur de la propriété **userFlags** de l’objet User.</span><span class="sxs-lookup"><span data-stu-id="10ca7-108">To determine if the user has been granted this permission with the WinNT provider, read the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of the user object.</span></span> <span data-ttu-id="10ca7-109">L’indicateur de **\_ \_ \_ \_ modification de décantation** de la balise de publicité uf est défini dans l’énumération enum de l' [**\_ \_ indicateur \_ utilisateur ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .</span><span class="sxs-lookup"><span data-stu-id="10ca7-109">The **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag is defined in the [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) enumeration.</span></span>

## <a name="example-code"></a><span data-ttu-id="10ca7-110">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="10ca7-110">Example Code</span></span>

<span data-ttu-id="10ca7-111">L’exemple de code suivant montre comment obtenir l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10ca7-111">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
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
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



<span data-ttu-id="10ca7-112">L’exemple de code suivant montre comment obtenir l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10ca7-112">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

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
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




