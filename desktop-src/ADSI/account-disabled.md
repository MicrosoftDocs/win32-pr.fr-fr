---
title: Compte désactivé (fournisseur LDAP)
description: Pour désactiver un compte d’utilisateur, affectez la valeur TRUE à la propriété AccountDisabled dans l’interface IADsUser. Cela est similaire au fournisseur Winnt. Les exemples de code suivants montrent comment désactiver un compte d’utilisateur.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Compte désactivé ADSI, fournisseur LDAP
- ADSI Provider ADSI, gestion des utilisateurs, exemples, compte désactivé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf753da0770e19504d496be20ba350f79bd4788a797eb5241e68261df844b626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181443"
---
# <a name="account-disabled-ldap-provider"></a>Compte désactivé (fournisseur LDAP)

Pour désactiver un compte d’utilisateur, affectez la **valeur true** à la propriété AccountDisabled dans l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . Cela est similaire au fournisseur Winnt. Les exemples de code suivants montrent comment désactiver un compte d’utilisateur.

## <a name="example-1"></a>Exemple 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>Exemple 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




