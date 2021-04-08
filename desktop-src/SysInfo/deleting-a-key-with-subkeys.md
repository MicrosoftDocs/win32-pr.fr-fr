---
description: L’exemple de cette rubrique utilise les fonctions RegOpenKeyEx, RegEnumKeyEx et RegDeleteKey pour supprimer une clé de Registre avec des sous-clés.
ms.assetid: 1cf6db95-85a4-4416-b17e-e14f45804503
title: Suppression d’une clé avec des sous-clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490020ff5a7bc6ea44f83b729bcbad4491aaa62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042875"
---
# <a name="deleting-a-key-with-subkeys"></a><span data-ttu-id="0768c-103">Suppression d’une clé avec des sous-clés</span><span class="sxs-lookup"><span data-stu-id="0768c-103">Deleting a Key with Subkeys</span></span>

<span data-ttu-id="0768c-104">L’exemple de cette rubrique utilise les fonctions [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa), [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)et [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) pour supprimer une clé de Registre avec des sous-clés.</span><span class="sxs-lookup"><span data-stu-id="0768c-104">The example in this topic uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa), [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa), and [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) functions to delete a registry key with subkeys.</span></span>

<span data-ttu-id="0768c-105">Pour tester cet exemple, créez la clé de Registre suivante à l’aide de Regedt32.exe, puis ajoutez les valeurs et les sous-clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="0768c-105">To test this example, create the following registry key by using Regedt32.exe, and then add a few values and subkeys:</span></span>

<span data-ttu-id="0768c-106">**HKEY \_ \_** TestDir du \\ **logiciel** \\  de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="0768c-106">**HKEY\_CURRENT\_USER**\\**Software**\\**TestDir**</span></span>

<span data-ttu-id="0768c-107">Après avoir exécuté le code, utilisez la touche F5 pour actualiser les données du Registre et notez que la clé **TestDir** est supprimée.</span><span class="sxs-lookup"><span data-stu-id="0768c-107">After running the code, use the F5 key to refresh the registry data, and notice that the **TestDir** key is deleted.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

//*************************************************************
//
//  RegDelnodeRecurse()
//
//  Purpose:    Deletes a registry key and all its subkeys / values.
//
//  Parameters: hKeyRoot    -   Root key
//              lpSubKey    -   SubKey to delete
//
//  Return:     TRUE if successful.
//              FALSE if an error occurs.
//
//*************************************************************

BOOL RegDelnodeRecurse (HKEY hKeyRoot, LPTSTR lpSubKey)
{
    LPTSTR lpEnd;
    LONG lResult;
    DWORD dwSize;
    TCHAR szName[MAX_PATH];
    HKEY hKey;
    FILETIME ftWrite;

    // First, see if we can delete the key without having
    // to recurse.

    lResult = RegDeleteKey(hKeyRoot, lpSubKey);

    if (lResult == ERROR_SUCCESS) 
        return TRUE;

    lResult = RegOpenKeyEx (hKeyRoot, lpSubKey, 0, KEY_READ, &hKey);

    if (lResult != ERROR_SUCCESS) 
    {
        if (lResult == ERROR_FILE_NOT_FOUND) {
            printf("Key not found.\n");
            return TRUE;
        } 
        else {
            printf("Error opening key.\n");
            return FALSE;
        }
    }

    // Check for an ending slash and add one if it is missing.

    lpEnd = lpSubKey + lstrlen(lpSubKey);

    if (*(lpEnd - 1) != TEXT('\\')) 
    {
        *lpEnd =  TEXT('\\');
        lpEnd++;
        *lpEnd =  TEXT('\0');
    }

    // Enumerate the keys

    dwSize = MAX_PATH;
    lResult = RegEnumKeyEx(hKey, 0, szName, &dwSize, NULL,
                           NULL, NULL, &ftWrite);

    if (lResult == ERROR_SUCCESS) 
    {
        do {

            *lpEnd = TEXT('\0');
            StringCchCat(lpSubKey, MAX_PATH * 2, szName);

            if (!RegDelnodeRecurse(hKeyRoot, lpSubKey)) {
                break;
            }

            dwSize = MAX_PATH;

            lResult = RegEnumKeyEx(hKey, 0, szName, &dwSize, NULL,
                                   NULL, NULL, &ftWrite);

        } while (lResult == ERROR_SUCCESS);
    }

    lpEnd--;
    *lpEnd = TEXT('\0');

    RegCloseKey (hKey);

    // Try again to delete the key.

    lResult = RegDeleteKey(hKeyRoot, lpSubKey);

    if (lResult == ERROR_SUCCESS) 
        return TRUE;

    return FALSE;
}

//*************************************************************
//
//  RegDelnode()
//
//  Purpose:    Deletes a registry key and all its subkeys / values.
//
//  Parameters: hKeyRoot    -   Root key
//              lpSubKey    -   SubKey to delete
//
//  Return:     TRUE if successful.
//              FALSE if an error occurs.
//
//*************************************************************

BOOL RegDelnode (HKEY hKeyRoot, LPCTSTR lpSubKey)
{
    TCHAR szDelKey[MAX_PATH*2];

    StringCchCopy (szDelKey, MAX_PATH*2, lpSubKey);
    return RegDelnodeRecurse(hKeyRoot, szDelKey);

}

int __cdecl main()
{
   BOOL bSuccess;

   bSuccess = RegDelnode(HKEY_CURRENT_USER, TEXT("Software\\TestDir"));

   if(bSuccess)
      printf("Success!\n");
   else printf("Failure.\n");

   return 0;
}
```



 

 



