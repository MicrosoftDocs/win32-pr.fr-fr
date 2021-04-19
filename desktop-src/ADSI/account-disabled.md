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
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106527085"
---
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="84826-107">Compte désactivé (fournisseur LDAP)</span><span class="sxs-lookup"><span data-stu-id="84826-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="84826-108">Pour désactiver un compte d’utilisateur, affectez la **valeur true** à la propriété AccountDisabled dans l’interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="84826-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="84826-109">Cela est similaire au fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="84826-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="84826-110">Les exemples de code suivants montrent comment désactiver un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84826-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="84826-111">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="84826-111">Example 1</span></span>


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



## <a name="example-2"></a><span data-ttu-id="84826-112">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="84826-112">Example 2</span></span>


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



 

 




