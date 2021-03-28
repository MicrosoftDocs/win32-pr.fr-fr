---
description: Vous avez maintenant tous les éléments essentiels nécessaires pour naviguer n’importe où dans l’espace de noms.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navigation dans l’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034098"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="517ee-103">Navigation dans l’espace de noms</span><span class="sxs-lookup"><span data-stu-id="517ee-103">Navigating the Namespace</span></span>

<span data-ttu-id="517ee-104">Vous avez maintenant tous les éléments essentiels nécessaires pour naviguer n’importe où dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="517ee-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="517ee-105">La façon la plus simple de commencer est de faire en sorte que votre application appelle [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) pour récupérer l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du bureau.</span><span class="sxs-lookup"><span data-stu-id="517ee-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="517ee-106">Ensuite, pour naviguer vers le bas de l’espace de noms, votre application peut suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="517ee-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="517ee-107">Énumérer le contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="517ee-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="517ee-108">Déterminez les objets qui sont des sous-dossiers, puis sélectionnez-en un.</span><span class="sxs-lookup"><span data-stu-id="517ee-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="517ee-109">Établissez une liaison avec le sous-dossier pour récupérer son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="517ee-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="517ee-110">Répétez ces étapes autant de fois que nécessaire pour atteindre la cible.</span><span class="sxs-lookup"><span data-stu-id="517ee-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="517ee-111">Exemple simple de navigation dans les espaces de noms</span><span class="sxs-lookup"><span data-stu-id="517ee-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="517ee-112">L’exemple de code suivant est une application console simple qui illustre un certain nombre de procédures présentées dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="517ee-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="517ee-113">La vérification des erreurs a été omise par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="517ee-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="517ee-114">L’application effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="517ee-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="517ee-115">Récupère l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier Program Files ([à l’aide de l’interface IShellFolder](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="517ee-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="517ee-116">Énumère le contenu du dossier ([énumération du contenu d’un dossier](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="517ee-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="517ee-117">Détermine tous les noms complets et les affiche (en[déterminant les noms d’affichage et d’autres propriétés](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="517ee-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="517ee-118">Recherche un sous-dossier ([en obtenant un pointeur vers l’interface IShellFolder d’un sous-dossier](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="517ee-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="517ee-119">Crée une liaison avec le premier sous-dossier trouvé ([en obtenant un pointeur vers l’interface IShellFolder d’un sous-dossier](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="517ee-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="517ee-120">Imprime les noms d’affichage des objets dans le sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="517ee-120">Prints the display names of the objects in the subfolder.</span></span>


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 
