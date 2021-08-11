---
title: Compte désactivé (fournisseur WinNT)
description: Lorsque vous utilisez le fournisseur WinNT, un compte peut être activé ou désactivé à l’aide de la propriété IADsUser. AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Compte désactivé (fournisseur WinNT)
- Compte désactivé ADSI, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, compte désactivé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1659bad4ab930615aed7d02e3c54fc3899b60eb476999676ff765fe2a2e94f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178504"
---
# <a name="account-disabled-winnt-provider"></a>Compte désactivé (fournisseur WinNT)

Lorsque vous utilisez le fournisseur WinNT, un compte peut être activé ou désactivé à l’aide de la propriété [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) .

## <a name="example-1"></a>Exemple 1

l’exemple de code suivant montre comment désactiver un compte à l’aide de Visual Basic avec ADSI.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Exemple 2

L’exemple de code suivant montre comment désactiver un compte à l’aide de C++ avec ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




