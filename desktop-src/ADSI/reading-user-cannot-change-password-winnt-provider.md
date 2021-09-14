---
title: La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur WinNT)
description: Découvrez comment déterminer si un utilisateur est autorisé à modifier un mot de passe pour le fournisseur Winnt. La capacité d’un utilisateur à modifier un mot de passe peut être accordée ou refusée.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- La lecture de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT) ADSI
- L’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT) ADSI, lecture
- ADSI Provider ADSI, exemples de gestion des utilisateurs, utilisateur ne peut pas modifier le mot de passe, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195748"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>La lecture de l’utilisateur ne peut pas changer le mot de passe (fournisseur WinNT)

La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée. Pour déterminer si cette autorisation a été accordée à l’utilisateur avec le fournisseur WinNT, lisez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur de la propriété **userFlags** de l’objet User. L’indicateur de **\_ \_ \_ \_ modification de décantation** de la balise de publicité uf est défini dans l’énumération enum de l' [**\_ \_ indicateur \_ utilisateur ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .

## <a name="example-code"></a>Exemple de code

L’exemple de code suivant montre comment obtenir l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.


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



L’exemple de code suivant montre comment obtenir l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.


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



 

 




