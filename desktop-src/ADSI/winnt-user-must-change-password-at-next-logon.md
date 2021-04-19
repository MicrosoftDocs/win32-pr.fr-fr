---
title: L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT)
description: Pour activer cette option, affectez la valeur 1 à l’attribut PasswordExpired de l’utilisateur. L’affectation de la valeur zéro (0) à cet attribut permet à l’utilisateur de se connecter sans modifier le mot de passe.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT) ADSI
- L’utilisateur doit changer de mot de passe à la prochaine ouverture de session ADSI, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, l’utilisateur doit changer de mot de passe à la prochaine ouverture de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106545879"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="4f6cd-107">L’utilisateur doit changer de mot de passe à la prochaine ouverture de session (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="4f6cd-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="4f6cd-108">Pour activer cette option, affectez la valeur 1 à l’attribut **PasswordExpired** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f6cd-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="4f6cd-109">L’affectation de la valeur zéro (0) à cet attribut permet à l’utilisateur de se connecter sans modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4f6cd-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="4f6cd-110">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="4f6cd-110">Example 1</span></span>

<span data-ttu-id="4f6cd-111">L’exemple de code suivant montre comment définir l’option modifier le mot de passe lors de la prochaine ouverture de session à l’aide de Visual Basic avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="4f6cd-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="4f6cd-112">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="4f6cd-112">Example 2</span></span>

<span data-ttu-id="4f6cd-113">L’exemple de code suivant montre comment définir l’option modifier le mot de passe pour la prochaine ouverture de session à l’aide de C++ avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="4f6cd-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




