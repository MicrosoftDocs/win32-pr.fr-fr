---
title: Exemple de boîte de dialogue Ouvrir
description: L’exemple Shapes que nous utilisons est quelque peu fictif. Passons à un objet COM que vous pouvez utiliser dans un programme Windows réel dans la boîte de dialogue Ouvrir.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381921"
---
# <a name="example-the-open-dialog-box"></a>Exemple : la boîte de dialogue Ouvrir

L' `Shapes` exemple que nous utilisons est quelque peu fictif. Passons à un objet COM que vous pouvez utiliser dans un programme Windows réel : la boîte de dialogue **ouvrir** .

![capture d’écran montrant la boîte de dialogue Ouvrir](images/fileopen01.png)

Pour afficher la boîte de dialogue **ouvrir** , un programme peut utiliser un objet COM appelé objet de boîte de dialogue élément commun. La boîte de dialogue élément commun implémente une interface nommée [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), qui est déclarée dans le fichier d’en-tête ShObjIdl. h.

Voici un programme qui affiche la boîte de dialogue **ouvrir** pour l’utilisateur. Si l’utilisateur sélectionne un fichier, le programme affiche une boîte de dialogue qui contient le nom du fichier.


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



Ce code utilise certains concepts qui seront décrits plus loin dans le module, donc ne vous inquiétez pas si vous ne comprenez pas tout cela ici. Voici un plan de base du code :

1.  Appelez [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.
2.  Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’objet de boîte de dialogue d’élément commun et obtenir un pointeur vers l’interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) de l’objet.
3.  Appelez la méthode **Show** de l’objet, qui affiche la boîte de dialogue à l’utilisateur. Cette méthode bloque jusqu’à ce que l’utilisateur ignore la boîte de dialogue.
4.  Appelez la méthode [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) de l’objet. Cette méthode retourne un pointeur vers un deuxième objet COM, appelé objet d' *élément de Shell* . L’élément de Shell, qui implémente l’interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , représente le fichier sélectionné par l’utilisateur.
5.  Appelez la méthode [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) de l’élément de Shell. Cette méthode obtient le chemin d’accès au fichier, sous la forme d’une chaîne.
6.  Affichez une boîte de message qui affiche le chemin d’accès du fichier.
7.  Appelez [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) pour désinitialiser la bibliothèque com.

Les étapes 1, 2 et 7 appellent les fonctions définies par la bibliothèque COM. Il s’agit de fonctions COM génériques. Les étapes 3 à 5 appellent des méthodes qui sont définies par l’objet de boîte de dialogue d’élément commun.

Cet exemple montre les deux variétés de création d’objets : la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) générique et une méthode ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) qui est spécifique à l’objet de boîte de dialogue d’élément commun.

## <a name="next"></a>Suivant

[Gestion de la durée de vie d’un objet](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ouvrir l’exemple de boîte de dialogue](open-dialog-box-sample.md)
</dt> </dl>

 

 