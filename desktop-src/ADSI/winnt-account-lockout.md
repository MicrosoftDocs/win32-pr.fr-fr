---
title: Verrouillage de compte (fournisseur WinNT)
description: Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant le nombre de minutes spécifié par l’attribut lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Verrouillage de compte ADSI, fournisseur Winnt
- ADSI Provider ADSI, exemples de gestion des utilisateurs, verrouillage de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511318"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="66c09-105">Verrouillage de compte (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="66c09-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="66c09-106">Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant le nombre de minutes spécifié par l’attribut [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="66c09-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="66c09-107">La propriété [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) semble être la propriété à utiliser pour lire et modifier l’état de verrouillage d’un compte d’utilisateur, mais le fournisseur ADSI Winnt a des restrictions qui limitent l’utilisation de la propriété **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="66c09-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="66c09-108">Réinitialisation de l’état de verrouillage de compte</span><span class="sxs-lookup"><span data-stu-id="66c09-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="66c09-109">Lorsque vous utilisez le fournisseur WinNT, la propriété [**IsAccountLocked**](iadsuser-property-methods.md) peut uniquement avoir la valeur **false**, ce qui déverrouille le compte.</span><span class="sxs-lookup"><span data-stu-id="66c09-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="66c09-110">Toute tentative d’affecter la valeur **true** à la propriété **IsAccountLocked** échouera.</span><span class="sxs-lookup"><span data-stu-id="66c09-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="66c09-111">Seul le système peut verrouiller un compte.</span><span class="sxs-lookup"><span data-stu-id="66c09-111">Only the system can lock an account.</span></span>

<span data-ttu-id="66c09-112">L’exemple de code suivant montre comment utiliser Visual Basic avec ADSI pour déverrouiller un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66c09-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



<span data-ttu-id="66c09-113">L’exemple de code suivant montre comment utiliser C++ avec ADSI pour déverrouiller un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66c09-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="66c09-114">Lecture de l’état de verrouillage de compte</span><span class="sxs-lookup"><span data-stu-id="66c09-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="66c09-115">Avec le fournisseur WinNT, la propriété [**IsAccountLocked**](iadsuser-property-methods.md) peut être utilisée pour déterminer si un compte est verrouillé. Si un compte est verrouillé, la propriété **IsAccountLocked** contient la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="66c09-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="66c09-116">Si un compte n’est pas verrouillé, la propriété **IsAccountLocked** contient la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="66c09-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="66c09-117">L’exemple de code suivant montre comment utiliser Visual Basic avec ADSI pour déterminer si un compte est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="66c09-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="66c09-118">L’exemple de code suivant montre comment utiliser C++ avec ADSI pour déterminer si un compte est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="66c09-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 