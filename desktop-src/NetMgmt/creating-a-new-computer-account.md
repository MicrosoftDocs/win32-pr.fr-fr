---
title: Création d’un compte d’ordinateur
description: L’exemple de code suivant montre comment créer un nouveau compte d’ordinateur à l’aide de la fonction NetUserAdd.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512320"
---
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="6e03f-103">Création d’un compte d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="6e03f-103">Creating a New Computer Account</span></span>

<span data-ttu-id="6e03f-104">L’exemple de code suivant montre comment créer un nouveau compte d’ordinateur à l’aide de la fonction [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .</span><span class="sxs-lookup"><span data-stu-id="6e03f-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="6e03f-105">Voici quelques éléments à prendre en compte pour la gestion des comptes d’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="6e03f-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="6e03f-106">Le nom du compte d’ordinateur doit être en majuscules pour assurer la cohérence avec les utilitaires de gestion des comptes.</span><span class="sxs-lookup"><span data-stu-id="6e03f-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="6e03f-107">Un nom de compte d’ordinateur comporte toujours un signe dollar ($) de fin.</span><span class="sxs-lookup"><span data-stu-id="6e03f-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="6e03f-108">Toutes les fonctions utilisées pour gérer les comptes d’ordinateur doivent créer le nom de l’ordinateur de sorte que le dernier caractère du nom du compte d’ordinateur soit le signe dollar ($).</span><span class="sxs-lookup"><span data-stu-id="6e03f-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="6e03f-109">Pour l’approbation interdomaine, le nom du compte est TrustingDomainName $.</span><span class="sxs-lookup"><span data-stu-id="6e03f-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="6e03f-110">La longueur maximale du nom d’ordinateur \_ est \_ longueur maximale de nom_ordinateur (15).</span><span class="sxs-lookup"><span data-stu-id="6e03f-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="6e03f-111">Cette longueur n’inclut pas le signe dollar ($) de fin.</span><span class="sxs-lookup"><span data-stu-id="6e03f-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="6e03f-112">Le mot de passe d’un nouveau compte d’ordinateur doit être la représentation en minuscules du nom du compte d’ordinateur, sans le signe dollar ($) final.</span><span class="sxs-lookup"><span data-stu-id="6e03f-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="6e03f-113">Pour l’approbation interdomaine, le mot de passe peut être une valeur arbitraire qui correspond à la valeur spécifiée côté approbation de la relation.</span><span class="sxs-lookup"><span data-stu-id="6e03f-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="6e03f-114">La longueur maximale du mot de passe est LM20 \_ PWLEN (14).</span><span class="sxs-lookup"><span data-stu-id="6e03f-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="6e03f-115">Le mot de passe doit être tronqué à cette longueur si le nom du compte d’ordinateur dépasse cette longueur.</span><span class="sxs-lookup"><span data-stu-id="6e03f-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="6e03f-116">Le mot de passe fourni lors de la création du compte d’ordinateur est valide uniquement jusqu’à ce que le compte d’ordinateur devienne actif sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="6e03f-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="6e03f-117">Un nouveau mot de passe est établi lors de l’activation de la relation d’approbation.</span><span class="sxs-lookup"><span data-stu-id="6e03f-117">A new password is established during trust relationship activation.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



<span data-ttu-id="6e03f-118">L’utilisateur qui appelle les fonctions de gestion de compte doit disposer de privilèges d’administrateur sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="6e03f-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="6e03f-119">Dans le cas des comptes d’ordinateurs existants, le créateur du compte peut gérer le compte, indépendamment de l’appartenance administrative.</span><span class="sxs-lookup"><span data-stu-id="6e03f-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="6e03f-120">Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="6e03f-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="6e03f-121">Le SeMachineAccountPrivilege peut être accordé sur l’ordinateur cible pour permettre aux utilisateurs spécifiés de créer des comptes d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e03f-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="6e03f-122">Cela permet aux non-administrateurs de créer des comptes d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e03f-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="6e03f-123">L’appelant doit activer ce privilège avant d’ajouter le compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e03f-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="6e03f-124">Pour plus d’informations sur les privilèges de compte, consultez [privilèges](/windows/desktop/SecAuthZ/privileges) et [constantes d’autorisation](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="6e03f-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 