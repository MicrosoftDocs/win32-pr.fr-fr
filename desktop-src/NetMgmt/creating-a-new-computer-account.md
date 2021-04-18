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
# <a name="creating-a-new-computer-account"></a>Création d’un compte d’ordinateur

L’exemple de code suivant montre comment créer un nouveau compte d’ordinateur à l’aide de la fonction [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .

Voici quelques éléments à prendre en compte pour la gestion des comptes d’ordinateur :

-   Le nom du compte d’ordinateur doit être en majuscules pour assurer la cohérence avec les utilitaires de gestion des comptes.
-   Un nom de compte d’ordinateur comporte toujours un signe dollar ($) de fin. Toutes les fonctions utilisées pour gérer les comptes d’ordinateur doivent créer le nom de l’ordinateur de sorte que le dernier caractère du nom du compte d’ordinateur soit le signe dollar ($). Pour l’approbation interdomaine, le nom du compte est TrustingDomainName $.
-   La longueur maximale du nom d’ordinateur \_ est \_ longueur maximale de nom_ordinateur (15). Cette longueur n’inclut pas le signe dollar ($) de fin.
-   Le mot de passe d’un nouveau compte d’ordinateur doit être la représentation en minuscules du nom du compte d’ordinateur, sans le signe dollar ($) final. Pour l’approbation interdomaine, le mot de passe peut être une valeur arbitraire qui correspond à la valeur spécifiée côté approbation de la relation.
-   La longueur maximale du mot de passe est LM20 \_ PWLEN (14). Le mot de passe doit être tronqué à cette longueur si le nom du compte d’ordinateur dépasse cette longueur.
-   Le mot de passe fourni lors de la création du compte d’ordinateur est valide uniquement jusqu’à ce que le compte d’ordinateur devienne actif sur le domaine. Un nouveau mot de passe est établi lors de l’activation de la relation d’approbation.


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



L’utilisateur qui appelle les fonctions de gestion de compte doit disposer de privilèges d’administrateur sur l’ordinateur cible. Dans le cas des comptes d’ordinateurs existants, le créateur du compte peut gérer le compte, indépendamment de l’appartenance administrative. Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

Le SeMachineAccountPrivilege peut être accordé sur l’ordinateur cible pour permettre aux utilisateurs spécifiés de créer des comptes d’ordinateur. Cela permet aux non-administrateurs de créer des comptes d’ordinateur. L’appelant doit activer ce privilège avant d’ajouter le compte d’ordinateur. Pour plus d’informations sur les privilèges de compte, consultez [privilèges](/windows/desktop/SecAuthZ/privileges) et [constantes d’autorisation](/windows/desktop/SecAuthZ/authorization-constants).

 

 