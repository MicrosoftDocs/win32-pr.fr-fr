---
title: Le mot de passe n’expire jamais (fournisseur WinNT)
description: Pour activer cette option à l’aide du fournisseur ADSI WinNT, définissez l' \_ indicateur ADS UF \_ \_ nopirer \_ passwd (0x10000) sur l’attribut userFlags. Remarque pour Windows 2000 et versions ultérieures, utilisez le fournisseur ADSI LDAP pour les opérations de gestion des utilisateurs, comme indiqué.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Le mot de passe n’expire jamais (fournisseur WinNT)
- Le mot de passe n’expire jamais ADSI, le fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, mot de passe n’expire jamais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106538309"
---
# <a name="password-never-expires-winnt-provider"></a><span data-ttu-id="e1544-106">Le mot de passe n’expire jamais (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="e1544-106">Password Never Expires (WinNT Provider)</span></span>

<span data-ttu-id="e1544-107">Pour activer cette option à l’aide du fournisseur ADSI WinNT, définissez l’indicateur **ADS \_ UF \_ \_ nopirer \_ passwd** (0x10000) sur l’attribut **userFlags** .</span><span class="sxs-lookup"><span data-stu-id="e1544-107">To enable this option using the WinNT ADSI provider, set the **ADS\_UF\_DONT\_EXPIRE\_PASSWD** (0x10000) flag on the **UserFlags** attribute.</span></span>

> [!Note]  
> <span data-ttu-id="e1544-108">Pour Windows 2000 et versions ultérieures, utilisez le fournisseur ADSI LDAP pour les opérations de gestion des utilisateurs, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="e1544-108">For Windows 2000 and later, use the LDAP ADSI provider for user management operations as shown.</span></span> <span data-ttu-id="e1544-109">Pour plus d’informations, consultez [mot de passe n’expire jamais (fournisseur LDAP)](password-never-expires.md).</span><span class="sxs-lookup"><span data-stu-id="e1544-109">For more information, see [Password Never Expires (LDAP Provider)](password-never-expires.md).</span></span>

 

## <a name="example-1"></a><span data-ttu-id="e1544-110">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e1544-110">Example 1</span></span>

<span data-ttu-id="e1544-111">L’exemple de code suivant montre comment définir l’option le mot de passe n’expire jamais à l’aide de Visual Basic avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="e1544-111">The following code example shows how to set the password never expires option using Visual Basic with ADSI.</span></span>


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="e1544-112">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e1544-112">Example 2</span></span>

<span data-ttu-id="e1544-113">L’exemple de code suivant montre comment définir l’option le mot de passe n’expire jamais à l’aide de C++ avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="e1544-113">The following code example shows how to set the password never expires option using C++ with ADSI.</span></span>


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




