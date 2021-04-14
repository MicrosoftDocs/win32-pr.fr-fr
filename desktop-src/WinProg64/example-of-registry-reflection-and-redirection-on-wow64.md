---
title: Exemple de redirection du Registre sur WOW64
description: L’exemple de code suivant illustre les vues distinctes du Registre fournies par le redirecteur du Registre sur Windows 64 bits.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- exemples de programmation Windows de 64 bits
- Guide de programmation Windows 64 bits exemples de programmation Windows 64 bits
- Guide de programmation Windows 64 bits exemples de programmation Windows 64 bits, redirection de Registre sur WOW64
- exemple de redirection de Registre, programmation Windows 64 bits
- Guide de programmation Windows 64 bits, programmation Windows 64 bits, exemples voir Guide de programmation Windows 64 bits exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff37b077137e9802e6716319623fe8e372941500
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104383148"
---
# <a name="example-of-registry-redirection-on-wow64"></a><span data-ttu-id="711e3-108">Exemple de redirection du Registre sur WOW64</span><span class="sxs-lookup"><span data-stu-id="711e3-108">Example of Registry Redirection on WOW64</span></span>

<span data-ttu-id="711e3-109">L’exemple de code suivant illustre les vues distinctes du Registre fournies par le redirecteur du Registre sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="711e3-109">The following example code demonstrates the separate views of the registry provided by the registry redirector on 64-bit Windows.</span></span> <span data-ttu-id="711e3-110">Il montre également comment les valeurs des clés sont définies selon qu’une clé est partagée ou redirigée.</span><span class="sxs-lookup"><span data-stu-id="711e3-110">It also demonstrates how the values of keys are set depending on whether a key is shared or redirected.</span></span> <span data-ttu-id="711e3-111">Pour plus d’informations, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="711e3-111">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>

<span data-ttu-id="711e3-112">Compilez le code suivant séparément pour les fenêtres 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="711e3-112">Compile the following code separately for both 32-bit and 64-bit Windows.</span></span> <span data-ttu-id="711e3-113">Exécutez chaque fichier exécutable résultant sur Windows 64 bits et comparez la sortie.</span><span class="sxs-lookup"><span data-stu-id="711e3-113">Run each resulting executable file on 64-bit Windows and compare the output.</span></span> <span data-ttu-id="711e3-114">L’exemple de sortie pour les deux versions est indiqué sous le code source.</span><span class="sxs-lookup"><span data-stu-id="711e3-114">Sample output for both versions is listed below the source code.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



<span data-ttu-id="711e3-115">Quand la version 64 bits de l’exemple est exécutée, elle génère la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="711e3-115">When the 64-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="711e3-116">Les valeurs des vues par défaut et secondaires de **HKCR \\ Hello** sont les mêmes, car cette clé est partagée.</span><span class="sxs-lookup"><span data-stu-id="711e3-116">The values of both the default and alternate views of **HKCR\\Hello** are the same because this key is shared.</span></span> <span data-ttu-id="711e3-117">Les valeurs des autres clés diffèrent, car elles sont redirigées.</span><span class="sxs-lookup"><span data-stu-id="711e3-117">The values of the other keys differ because they are redirected.</span></span>

<span data-ttu-id="711e3-118">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Lorsque cet exemple est exécuté sur ces systèmes d’exploitation, les vues par défaut et secondaires de la clé LocalServer32 ont la même valeur.</span><span class="sxs-lookup"><span data-stu-id="711e3-118">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** When this example is run on these operating systems, the default and alternate views of the LocalServer32 key have the same value.</span></span> <span data-ttu-id="711e3-119">Cela est dû au fait que la clé LocalServer32 est redirigée et *réfléchie*, ce qui entraîne la synchronisation de sa valeur entre les vues 64 bits et 32 bits du Registre dès que le handle de la clé est fermé.</span><span class="sxs-lookup"><span data-stu-id="711e3-119">This is because the LocalServer32 key is redirected and *reflected*, which causes its value to be synchronized between the 64-bit and 32-bit views of the registry as soon as the handle to the key is closed.</span></span> <span data-ttu-id="711e3-120">La réflexion du registre a été supprimée à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="711e3-120">Registry reflection was removed starting with Windows 7.</span></span> <span data-ttu-id="711e3-121">Pour plus d’informations, consultez [Registry Reflection](registry-reflection.md).</span><span class="sxs-lookup"><span data-stu-id="711e3-121">For more information, see [Registry Reflection](registry-reflection.md).</span></span>

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

<span data-ttu-id="711e3-122">Quand la version 32 bits de l’exemple est exécutée, elle génère la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="711e3-122">When the 32-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="711e3-123">Pour une application 32 bits, la vue 64 bits du Registre est l’autre vue afin que les valeurs soient inversées, à l’exception de HKCR \\ Hello, qui est une clé partagée.</span><span class="sxs-lookup"><span data-stu-id="711e3-123">For a 32-bit application, the 64-bit view of the registry is the alternate view so the values are reversed, except for HKCR\\Hello, which is a shared key.</span></span>

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

<span data-ttu-id="711e3-124">Pour examiner l’effet de l’exécution de cet exemple avec regedit, examinez les valeurs des clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="711e3-124">To examine the effect of running this example with regedit, inspect the values of the following keys.</span></span> <span data-ttu-id="711e3-125">Notez que les applications doivent éviter d’utiliser Wow6432Node dans des chemins de Registre codés en dur.</span><span class="sxs-lookup"><span data-stu-id="711e3-125">Note that applications should avoid using Wow6432Node in hard-coded registry paths.</span></span>

<span data-ttu-id="711e3-126">**HKLM \\ SOFTWARE \\ Hello World**</span><span class="sxs-lookup"><span data-stu-id="711e3-126">**HKLM\\SOFTWARE\\Hello World**</span></span>  
<span data-ttu-id="711e3-127">**HKLM \\ Software \\ Wow6432Node \\ Hello World**</span><span class="sxs-lookup"><span data-stu-id="711e3-127">**HKLM\\SOFTWARE\\Wow6432Node\\Hello World**</span></span>  
<span data-ttu-id="711e3-128">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="711e3-128">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="711e3-129">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="711e3-129">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="711e3-130">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="711e3-130">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="711e3-131">**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="711e3-131">**HKCR\\Hello HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="711e3-132">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="711e3-132">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="711e3-133">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="711e3-133">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="711e3-134">**HKCR \\ Wow6432Node \\ Hello**</span><span class="sxs-lookup"><span data-stu-id="711e3-134">**HKCR\\Wow6432Node\\Hello**</span></span>  


## <a name="related-topics"></a><span data-ttu-id="711e3-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="711e3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="711e3-136">Redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="711e3-136">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="711e3-137">Réflexion du Registre</span><span class="sxs-lookup"><span data-stu-id="711e3-137">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 




