---
description: Chaque processus est associé à un bloc d’environnement.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Modification des variables d’environnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544853"
---
# <a name="changing-environment-variables"></a><span data-ttu-id="662b9-103">Modification des variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="662b9-103">Changing Environment Variables</span></span>

<span data-ttu-id="662b9-104">Chaque processus est associé à un bloc d’environnement.</span><span class="sxs-lookup"><span data-stu-id="662b9-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="662b9-105">Le bloc environnement se compose d’un bloc se terminant par un caractère null de chaînes se terminant par un caractère null (ce qui signifie qu’il y a deux octets null à la fin du bloc), où chaque chaîne se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="662b9-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="662b9-106">*nom* = *valeur*</span><span class="sxs-lookup"><span data-stu-id="662b9-106">*name*=*value*</span></span>

<span data-ttu-id="662b9-107">Toutes les chaînes du bloc d’environnement doivent être triées par ordre alphabétique par nom.</span><span class="sxs-lookup"><span data-stu-id="662b9-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="662b9-108">Le tri ne respecte pas la casse, l’ordre Unicode, sans tenir compte des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="662b9-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="662b9-109">Étant donné que le signe égal est un séparateur, il ne doit pas être utilisé dans le nom d’une variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="662b9-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="662b9-110">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="662b9-110">Example 1</span></span>

<span data-ttu-id="662b9-111">Par défaut, un processus enfant hérite d’une copie du bloc d’environnement du processus parent.</span><span class="sxs-lookup"><span data-stu-id="662b9-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="662b9-112">L’exemple suivant montre comment créer un bloc d’environnement à passer à un processus enfant à l’aide de [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="662b9-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="662b9-113">Cet exemple utilise le code de l’exemple trois comme processus enfant, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="662b9-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a><span data-ttu-id="662b9-114">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="662b9-114">Example 2</span></span>

<span data-ttu-id="662b9-115">La modification des variables d’environnement d’un processus enfant lors de la création d’un processus est la seule façon de modifier directement les variables d’environnement d’un autre processus.</span><span class="sxs-lookup"><span data-stu-id="662b9-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="662b9-116">Un processus ne peut jamais modifier directement les variables d’environnement d’un autre processus qui n’est pas un enfant de ce processus.</span><span class="sxs-lookup"><span data-stu-id="662b9-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="662b9-117">Si vous souhaitez que le processus enfant hérite de la majeure partie de l’environnement du parent avec quelques modifications seulement, récupérez les valeurs actuelles à l’aide de [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), enregistrez ces valeurs, créez un bloc mis à jour pour que le processus enfant hérite, créez le processus enfant, puis restaurez les valeurs enregistrées à l’aide de [**SetEnvironmentVariable ne contient**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="662b9-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="662b9-118">Cet exemple utilise le code de l’exemple trois comme processus enfant, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="662b9-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a><span data-ttu-id="662b9-119">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="662b9-119">Example 3</span></span>

<span data-ttu-id="662b9-120">L’exemple suivant récupère le bloc d’environnement du processus à l’aide de [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) et imprime le contenu sur la console.</span><span class="sxs-lookup"><span data-stu-id="662b9-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
