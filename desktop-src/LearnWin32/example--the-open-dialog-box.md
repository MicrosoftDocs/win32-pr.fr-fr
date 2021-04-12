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
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="462c7-104">Exemple : la boîte de dialogue Ouvrir</span><span class="sxs-lookup"><span data-stu-id="462c7-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="462c7-105">L' `Shapes` exemple que nous utilisons est quelque peu fictif.</span><span class="sxs-lookup"><span data-stu-id="462c7-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="462c7-106">Passons à un objet COM que vous pouvez utiliser dans un programme Windows réel : la boîte de dialogue **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="462c7-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![capture d’écran montrant la boîte de dialogue Ouvrir](images/fileopen01.png)

<span data-ttu-id="462c7-108">Pour afficher la boîte de dialogue **ouvrir** , un programme peut utiliser un objet COM appelé objet de boîte de dialogue élément commun.</span><span class="sxs-lookup"><span data-stu-id="462c7-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="462c7-109">La boîte de dialogue élément commun implémente une interface nommée [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), qui est déclarée dans le fichier d’en-tête ShObjIdl. h.</span><span class="sxs-lookup"><span data-stu-id="462c7-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="462c7-110">Voici un programme qui affiche la boîte de dialogue **ouvrir** pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="462c7-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="462c7-111">Si l’utilisateur sélectionne un fichier, le programme affiche une boîte de dialogue qui contient le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="462c7-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


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



<span data-ttu-id="462c7-112">Ce code utilise certains concepts qui seront décrits plus loin dans le module, donc ne vous inquiétez pas si vous ne comprenez pas tout cela ici.</span><span class="sxs-lookup"><span data-stu-id="462c7-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="462c7-113">Voici un plan de base du code :</span><span class="sxs-lookup"><span data-stu-id="462c7-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="462c7-114">Appelez [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="462c7-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="462c7-115">Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’objet de boîte de dialogue d’élément commun et obtenir un pointeur vers l’interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="462c7-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="462c7-116">Appelez la méthode **Show** de l’objet, qui affiche la boîte de dialogue à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="462c7-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="462c7-117">Cette méthode bloque jusqu’à ce que l’utilisateur ignore la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="462c7-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="462c7-118">Appelez la méthode [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="462c7-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="462c7-119">Cette méthode retourne un pointeur vers un deuxième objet COM, appelé objet d' *élément de Shell* .</span><span class="sxs-lookup"><span data-stu-id="462c7-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="462c7-120">L’élément de Shell, qui implémente l’interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , représente le fichier sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="462c7-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="462c7-121">Appelez la méthode [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) de l’élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="462c7-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="462c7-122">Cette méthode obtient le chemin d’accès au fichier, sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="462c7-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="462c7-123">Affichez une boîte de message qui affiche le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="462c7-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="462c7-124">Appelez [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) pour désinitialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="462c7-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="462c7-125">Les étapes 1, 2 et 7 appellent les fonctions définies par la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="462c7-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="462c7-126">Il s’agit de fonctions COM génériques.</span><span class="sxs-lookup"><span data-stu-id="462c7-126">These are generic COM functions.</span></span> <span data-ttu-id="462c7-127">Les étapes 3 à 5 appellent des méthodes qui sont définies par l’objet de boîte de dialogue d’élément commun.</span><span class="sxs-lookup"><span data-stu-id="462c7-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="462c7-128">Cet exemple montre les deux variétés de création d’objets : la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) générique et une méthode ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) qui est spécifique à l’objet de boîte de dialogue d’élément commun.</span><span class="sxs-lookup"><span data-stu-id="462c7-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="462c7-129">Suivant</span><span class="sxs-lookup"><span data-stu-id="462c7-129">Next</span></span>

[<span data-ttu-id="462c7-130">Gestion de la durée de vie d’un objet</span><span class="sxs-lookup"><span data-stu-id="462c7-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="462c7-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="462c7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="462c7-132">Ouvrir l’exemple de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="462c7-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 