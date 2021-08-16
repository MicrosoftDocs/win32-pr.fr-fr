---
title: Expiration du compte (fournisseur WinNT)
description: Lorsque vous utilisez le fournisseur WinNT, vous pouvez définir la date d’expiration du compte à l’aide de la propriété IADsUser. AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- ADSI d’expiration de compte, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, expiration du compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd23973a4de31fed629428be9f4df1b6cade34e77f78680a5f87c9d55c42234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838409"
---
# <a name="account-expiration-winnt-provider"></a>Expiration du compte (fournisseur WinNT)

Lorsque vous utilisez le fournisseur WinNT, vous pouvez définir la date d’expiration du compte à l’aide de la propriété [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) .

Pour définir la date d’expiration du compte, affectez à la propriété [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) la valeur de date souhaitée. Pour définir la date d’expiration du compte de sorte qu’elle n’expire jamais, définissez cette propriété sur « 1er janvier 1970 ».

## <a name="example-1"></a>Exemple 1

l’exemple de code suivant montre comment définir la date d’expiration du compte à l’aide de Visual Basic avec ADSI.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Exemple 2

L’exemple de code suivant montre comment définir la date d’expiration du compte à l’aide de C++ avec ADSI.


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




