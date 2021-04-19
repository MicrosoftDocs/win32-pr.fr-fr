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
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106535152"
---
# <a name="account-expiration-winnt-provider"></a><span data-ttu-id="117fa-105">Expiration du compte (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="117fa-105">Account Expiration (WinNT Provider)</span></span>

<span data-ttu-id="117fa-106">Lorsque vous utilisez le fournisseur WinNT, vous pouvez définir la date d’expiration du compte à l’aide de la propriété [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="117fa-106">When using the WinNT provider, the account expiration date can be set using the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property.</span></span>

<span data-ttu-id="117fa-107">Pour définir la date d’expiration du compte, affectez à la propriété [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) la valeur de date souhaitée.</span><span class="sxs-lookup"><span data-stu-id="117fa-107">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="117fa-108">Pour définir la date d’expiration du compte de sorte qu’elle n’expire jamais, définissez cette propriété sur « 1er janvier 1970 ».</span><span class="sxs-lookup"><span data-stu-id="117fa-108">To set the account expiration date to never expire, set this property to "January 1, 1970".</span></span>

## <a name="example-1"></a><span data-ttu-id="117fa-109">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="117fa-109">Example 1</span></span>

<span data-ttu-id="117fa-110">L’exemple de code suivant montre comment définir la date d’expiration du compte à l’aide de Visual Basic avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="117fa-110">The following code example shows how to set the account expiration date using Visual Basic with ADSI.</span></span>


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="117fa-111">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="117fa-111">Example 2</span></span>

<span data-ttu-id="117fa-112">L’exemple de code suivant montre comment définir la date d’expiration du compte à l’aide de C++ avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="117fa-112">The following code example shows how to set the account expiration date using C++ with ADSI.</span></span>


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



 

 




