---
description: Vous avez maintenant tous les éléments essentiels nécessaires pour naviguer n’importe où dans l’espace de noms.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navigation dans l’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523340"
---
# <a name="navigating-the-namespace"></a>Navigation dans l’espace de noms

Vous avez maintenant tous les éléments essentiels nécessaires pour naviguer n’importe où dans l’espace de noms. La façon la plus simple de commencer est de faire en sorte que votre application appelle [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) pour récupérer l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du bureau. Ensuite, pour naviguer vers le bas de l’espace de noms, votre application peut suivre les étapes suivantes :

1.  Énumérer le contenu du dossier.
2.  Déterminez les objets qui sont des sous-dossiers, puis sélectionnez-en un.
3.  Établissez une liaison avec le sous-dossier pour récupérer son interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Répétez ces étapes autant de fois que nécessaire pour atteindre la cible.

## <a name="a-simple-example-of-namespace-navigation"></a>Exemple simple de navigation dans les espaces de noms

L’exemple de code suivant est une application console simple qui illustre un certain nombre de procédures présentées dans les sections précédentes. La vérification des erreurs a été omise par souci de clarté. L’application effectue les tâches suivantes :

1.  Récupère l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier Program Files ([à l’aide de l’interface IShellFolder](folder-info.md)).
2.  Énumère le contenu du dossier ([énumération du contenu d’un dossier](folder-info.md)).
3.  Détermine tous les noms complets et les affiche (en[déterminant les noms d’affichage et d’autres propriétés](folder-info.md)).
4.  Recherche un sous-dossier ([en obtenant un pointeur vers l’interface IShellFolder d’un sous-dossier](folder-info.md)).
5.  Crée une liaison avec le premier sous-dossier trouvé ([en obtenant un pointeur vers l’interface IShellFolder d’un sous-dossier](folder-info.md)).
6.  Imprime les noms d’affichage des objets dans le sous-dossier.


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



 

 
