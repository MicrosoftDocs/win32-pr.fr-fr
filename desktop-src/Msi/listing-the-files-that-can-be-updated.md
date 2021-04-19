---
description: La fonction MsiGetPatchFileList et la propriété PatchFiles de l’objet installer prennent la liste des correctifs Windows Installer (fichiers. msp) et retournent une liste des fichiers qui peuvent être mis à jour par les correctifs.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Liste des fichiers qui peuvent être mis à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c15872cce902f5a9059d4256e9e5c30ecff213f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544947"
---
# <a name="listing-the-files-that-can-be-updated"></a><span data-ttu-id="e80c7-103">Liste des fichiers qui peuvent être mis à jour</span><span class="sxs-lookup"><span data-stu-id="e80c7-103">Listing the Files that can be Updated</span></span>

<span data-ttu-id="e80c7-104">La fonction [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) et la propriété [**PatchFiles**](installer-patchfiles.md) de l' [**objet installer**](installer-object.md) prennent la liste des correctifs Windows Installer (fichiers. msp) et retournent une liste des fichiers qui peuvent être mis à jour par les correctifs.</span><span class="sxs-lookup"><span data-stu-id="e80c7-104">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md) take a list of Windows Installer patches (.msp files) and return a list of files that can be updated by the patches.</span></span> <span data-ttu-id="e80c7-105">La fonction [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) et la propriété [**PatchFiles**](installer-patchfiles.md) sont disponibles à partir de Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="e80c7-105">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property are available beginning with Windows Installer 4.0.</span></span>

## <a name="listing-files-that-can-be-updated"></a><span data-ttu-id="e80c7-106">Liste des fichiers qui peuvent être mis à jour</span><span class="sxs-lookup"><span data-stu-id="e80c7-106">Listing Files that can be Updated</span></span>

<span data-ttu-id="e80c7-107">L’exemple suivant montre comment extraire les informations d’applicabilité d’une liste de correctifs de Windows Installer (fichiers. msp) à l’aide de [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="e80c7-107">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="e80c7-108">La fonction **MsiGetPatchFileList** est fournie pour la cible des correctifs et une liste de fichiers. msp délimités par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e80c7-108">The **MsiGetPatchFileList** function is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="e80c7-109">Cet exemple nécessite Windows Installer 4,0 s’exécutant sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e80c7-109">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



<span data-ttu-id="e80c7-110">L’exemple suivant montre comment extraire les informations d’applicabilité d’une liste de Windows Installer correctifs (fichiers. msp) à l’aide de la propriété [**PatchFiles**](installer-patchfiles.md) de l' [**objet installer**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="e80c7-110">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="e80c7-111">La propriété **PatchFiles** est fournie dans le code de produit de la cible des correctifs et une liste de fichiers. msp délimités par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e80c7-111">The **PatchFiles** property is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="e80c7-112">Cet exemple nécessite Windows Installer 4,0 s’exécutant sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e80c7-112">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



