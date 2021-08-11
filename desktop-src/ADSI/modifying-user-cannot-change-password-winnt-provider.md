---
title: La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)
description: Découvrez comment refuser à un utilisateur l’autorisation de modifier un mot de passe pour le fournisseur Winnt. La capacité d’un utilisateur à modifier son propre mot de passe peut être accordée ou refusée.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)
- L’utilisateur ne peut pas changer de mot de passe (fournisseur WinNT), modification
- ADSI Provider ADSI, exemples de gestion des utilisateurs, utilisateur ne peut pas modifier le mot de passe, modifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b510fb08172a178a454ee731110765844368ca78108047a7a5a738b78b6a196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178963"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a>La modification de l’utilisateur ne peut pas modifier le mot de passe (fournisseur WinNT)

La possibilité pour un utilisateur de modifier son propre mot de passe est une autorisation qui peut être accordée ou refusée. Pour refuser cette autorisation, ajoutez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur à la propriété **userFlags** de l’objet User. Pour accorder cette autorisation, supprimez l’indicateur de **\_ \_ \_ \_ modification** de l’autorisation de l’utilisateur de la propriété **userFlags** de l’objet User.

## <a name="example-code"></a>Exemple de code

L’exemple de code suivant montre comment modifier l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.


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



L’exemple de code suivant montre comment modifier l’indicateur de **\_ \_ \_ \_ modification de décantation** de la propriété **userFlags** d’un objet utilisateur.


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



 

 




