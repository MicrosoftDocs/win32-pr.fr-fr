---
description: L’Explorateur Windows est une application puissante de navigation et de gestion des ressources.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Développement avec l’Explorateur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484385"
---
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="bc260-103">Développement avec l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="bc260-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="bc260-104">L’Explorateur Windows est une application puissante de navigation et de gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="bc260-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="bc260-105">L’Explorateur Windows est accessible en tant qu’ensemble intégré à Explorer.exe ou à l’interface [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="bc260-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="bc260-106">L’Explorateur Windows (Explorer.exe) peut être généré en tant que processus distinct à l’aide de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou d’une fonction similaire.</span><span class="sxs-lookup"><span data-stu-id="bc260-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="bc260-107">Les options de ligne de commande pour Explorer.exe sont documentées sur le site du support technique de Microsoft Windows dans l’article options d' Command-Line de l' [Explorateur Windows](https://support.microsoft.com/kb/152457).</span><span class="sxs-lookup"><span data-stu-id="bc260-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="bc260-108">Les fenêtres d’explorateur ouvertes peuvent être découvertes et programmées à l’aide de [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows), et de nouvelles instances de l’Explorateur Windows peuvent être créées à l’aide de [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).</span><span class="sxs-lookup"><span data-stu-id="bc260-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="bc260-109">L’exemple de code suivant montre comment le modèle Automation de l’Explorateur Windows peut être utilisé pour créer et découvrir des fenêtres Explorateur qui exécutent.</span><span class="sxs-lookup"><span data-stu-id="bc260-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="bc260-110">La zone cliente de l’Explorateur Windows peut être hébergée à l’aide de l’interface [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="bc260-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="bc260-111">Le client de l’Explorateur Windows et les contrôles d’arborescence de l’espace de noms sont des composants standard de Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc260-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="bc260-112">Les développeurs peuvent réutiliser les interfaces comme des composants de génération.</span><span class="sxs-lookup"><span data-stu-id="bc260-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="bc260-113">Ces contrôles sont couramment utilisés pour créer des explorateurs personnalisés appropriés au domaine du problème.</span><span class="sxs-lookup"><span data-stu-id="bc260-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="bc260-114">Les contrôles de l’Explorateur Windows sont classés dans les catégories fonctionnelles suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc260-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="bc260-115">Contrôles de navigation</span><span class="sxs-lookup"><span data-stu-id="bc260-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="bc260-116">Contrôles de commande</span><span class="sxs-lookup"><span data-stu-id="bc260-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="bc260-117">Contrôles de propriété et d’aperçu</span><span class="sxs-lookup"><span data-stu-id="bc260-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="bc260-118">Filtrage et affichage des contrôles</span><span class="sxs-lookup"><span data-stu-id="bc260-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="bc260-119">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="bc260-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="bc260-120">Contrôles de navigation</span><span class="sxs-lookup"><span data-stu-id="bc260-120">Navigation Controls</span></span>

<span data-ttu-id="bc260-121">Les contrôles de navigation aident les utilisateurs à déterminer le contexte et à naviguer dans l’espace de domaine logique associé, appelé espace.</span><span class="sxs-lookup"><span data-stu-id="bc260-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="bc260-122">Par exemple, le espace pour l’Explorateur Windows est l’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="bc260-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="bc260-123">Les espaces sont composés de zéro ou de plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="bc260-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="bc260-124">Le tableau suivant répertorie et décrit les contrôles de navigation disponibles dans l’Explorateur Windows dans les systèmes d’exploitation Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc260-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="bc260-125">Contrôle de navigation</span><span class="sxs-lookup"><span data-stu-id="bc260-125">Navigation control</span></span>               | <span data-ttu-id="bc260-126">Description</span><span class="sxs-lookup"><span data-stu-id="bc260-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc260-127">Barre d’adresses (contrôle de navigation)</span><span class="sxs-lookup"><span data-stu-id="bc260-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="bc260-128">Affiche l’adresse de la page actuelle dans le espace.</span><span class="sxs-lookup"><span data-stu-id="bc260-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="bc260-129">Vous pouvez cliquer sur les boutons de navigation pour accéder à n’importe quel ancêtre dans le espace.</span><span class="sxs-lookup"><span data-stu-id="bc260-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="bc260-130">Les utilisateurs peuvent également taper des URL et des chemins d’accès pour naviguer.</span><span class="sxs-lookup"><span data-stu-id="bc260-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="bc260-131">Arborescence des dossiers</span><span class="sxs-lookup"><span data-stu-id="bc260-131">Folder Tree</span></span>                      | <span data-ttu-id="bc260-132">Fournit une nouvelle version d’un contrôle d’arborescence, optimisé pour les grands espaces.</span><span class="sxs-lookup"><span data-stu-id="bc260-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="bc260-133">Voyage</span><span class="sxs-lookup"><span data-stu-id="bc260-133">Travel</span></span>                           | <span data-ttu-id="bc260-134">Active la navigation relative par le biais de boutons de style Web tels que **précédent** et **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc260-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="bc260-135">Intitulé</span><span class="sxs-lookup"><span data-stu-id="bc260-135">Title</span></span>                            | <span data-ttu-id="bc260-136">Affiche le nom et le contexte de l’Explorateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bc260-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="bc260-137">Espace</span><span class="sxs-lookup"><span data-stu-id="bc260-137">Pagespace</span></span>                        | <span data-ttu-id="bc260-138">Affiche la branche active de la espace.</span><span class="sxs-lookup"><span data-stu-id="bc260-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="bc260-139">Les pages peuvent être classées selon différents critères.</span><span class="sxs-lookup"><span data-stu-id="bc260-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="bc260-140">Les utilisateurs peuvent cliquer sur une page pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="bc260-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="bc260-141">Contrôles de commande</span><span class="sxs-lookup"><span data-stu-id="bc260-141">Command Controls</span></span>

<span data-ttu-id="bc260-142">Les contrôles de commande publient les fonctionnalités de l’Explorateur Windows pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bc260-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="bc260-143">Ces contrôles effectuent des actions générales ou des actions spécifiques à un ou plusieurs éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="bc260-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="bc260-144">Contrôle de commande</span><span class="sxs-lookup"><span data-stu-id="bc260-144">Command control</span></span> | <span data-ttu-id="bc260-145">Description</span><span class="sxs-lookup"><span data-stu-id="bc260-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc260-146">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="bc260-146">Toolbar</span></span>         | <span data-ttu-id="bc260-147">Affiche des boutons pour les commandes couramment utilisées (une nouvelle version d’une barre d’outils de commande).</span><span class="sxs-lookup"><span data-stu-id="bc260-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="bc260-148">Les options de personnalisation incluent des boutons déroulants, des boutons partagés, du texte descriptif facultatif et une zone de dépassement.</span><span class="sxs-lookup"><span data-stu-id="bc260-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="bc260-149">Bannière</span><span class="sxs-lookup"><span data-stu-id="bc260-149">Hero</span></span>            | <span data-ttu-id="bc260-150">S’affiche sous la forme d’un contrôle personnalisé unique, facultatif, au centre de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bc260-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="bc260-151">Il représente la commande principale pour le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="bc260-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="bc260-152">Barre de menus</span><span class="sxs-lookup"><span data-stu-id="bc260-152">Menu Bar</span></span>        | <span data-ttu-id="bc260-153">Présente les commandes dans les menus.</span><span class="sxs-lookup"><span data-stu-id="bc260-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="bc260-154">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="bc260-154">Context Menu</span></span>    | <span data-ttu-id="bc260-155">Répertorie un sous-ensemble approprié des commandes disponibles, qui s’affichent à la suite d’un clic droit sur un élément.</span><span class="sxs-lookup"><span data-stu-id="bc260-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="bc260-156">Contrôles de propriété et d’aperçu</span><span class="sxs-lookup"><span data-stu-id="bc260-156">Property and Preview Controls</span></span>

<span data-ttu-id="bc260-157">Les contrôles de propriété et d’aperçu permettent d’afficher un aperçu des éléments, ainsi que d’afficher et de modifier les propriétés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="bc260-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="bc260-158">Control</span><span class="sxs-lookup"><span data-stu-id="bc260-158">Control</span></span>    | <span data-ttu-id="bc260-159">Description</span><span class="sxs-lookup"><span data-stu-id="bc260-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc260-160">PRÉVERSION</span><span class="sxs-lookup"><span data-stu-id="bc260-160">Preview</span></span>    | <span data-ttu-id="bc260-161">Affiche un aperçu de l’élément sélectionné, tel qu’une miniature ou une icône en direct.</span><span class="sxs-lookup"><span data-stu-id="bc260-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="bc260-162">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc260-162">Properties</span></span> | <span data-ttu-id="bc260-163">Affiche les propriétés de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bc260-163">Displays properties of the selected item.</span></span> <span data-ttu-id="bc260-164">Pour les sélections multiples, elle affiche un résumé des propriétés pour le groupe d’éléments sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bc260-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="bc260-165">Pour une sélection null, elle affiche un résumé des propriétés de la page actuelle (contenu de ListView).</span><span class="sxs-lookup"><span data-stu-id="bc260-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="bc260-166">Filtrage et affichage des contrôles</span><span class="sxs-lookup"><span data-stu-id="bc260-166">Filtering and View Controls</span></span>

<span data-ttu-id="bc260-167">Les contrôles de filtrage et d’affichage permettent de manipuler l’ensemble des éléments de ListView et de modifier la présentation des éléments dans ListView.</span><span class="sxs-lookup"><span data-stu-id="bc260-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="bc260-168">Control</span><span class="sxs-lookup"><span data-stu-id="bc260-168">Control</span></span>   | <span data-ttu-id="bc260-169">Description</span><span class="sxs-lookup"><span data-stu-id="bc260-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc260-170">Filtrer</span><span class="sxs-lookup"><span data-stu-id="bc260-170">Filter</span></span>    | <span data-ttu-id="bc260-171">Filtre ou organise des éléments dans un ListView en fonction des propriétés listées en tant que colonnes.</span><span class="sxs-lookup"><span data-stu-id="bc260-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="bc260-172">Cliquer sur une colonne trie par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bc260-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="bc260-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="bc260-173">Wordwheel</span></span> | <span data-ttu-id="bc260-174">Filtre de façon dynamique et incrémentielle les éléments affichés dans un ListView en fonction d’une chaîne de texte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bc260-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="bc260-175">Affichage</span><span class="sxs-lookup"><span data-stu-id="bc260-175">View</span></span>      | <span data-ttu-id="bc260-176">Permet à l’utilisateur de modifier le mode d’affichage d’un contrôle ListView.</span><span class="sxs-lookup"><span data-stu-id="bc260-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="bc260-177">Un curseur peut être utilisé pour déterminer la taille des icônes.</span><span class="sxs-lookup"><span data-stu-id="bc260-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="bc260-178">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="bc260-178">Listview Control</span></span>

<span data-ttu-id="bc260-179">Le contrôle ListView est utilisé pour afficher un ensemble d’éléments dans l’un des quatre modes d’affichage suivants : détails, vignettes, icônes ou Panorama.</span><span class="sxs-lookup"><span data-stu-id="bc260-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="bc260-180">Le contrôle ListView permet également à l’utilisateur de sélectionner et d’activer un ou plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="bc260-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="bc260-181">Bien que certains de ces contrôles aient des noms et/ou des fonctionnalités qui sont similaires aux contrôles de Windows Presentation Foundation standard (WPF) présents dans l’espace de noms System. Windows. Controls, il s’agit de classes distinctes.</span><span class="sxs-lookup"><span data-stu-id="bc260-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="bc260-182">Ces contrôles distincts fonctionnent ensemble en grande partie par le biais d’événements générés par l’interaction de l’utilisateur ou par les contrôles eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="bc260-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="bc260-183">Le tableau suivant présente les trois principales catégories d’événements.</span><span class="sxs-lookup"><span data-stu-id="bc260-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="bc260-184">Catégorie d'événements</span><span class="sxs-lookup"><span data-stu-id="bc260-184">Event category</span></span> | <span data-ttu-id="bc260-185">Exemple</span><span class="sxs-lookup"><span data-stu-id="bc260-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="bc260-186">Navigation</span><span class="sxs-lookup"><span data-stu-id="bc260-186">Navigation</span></span>     | <span data-ttu-id="bc260-187">Passage d’une page à l’autre.</span><span class="sxs-lookup"><span data-stu-id="bc260-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="bc260-188">Sélection</span><span class="sxs-lookup"><span data-stu-id="bc260-188">Selection</span></span>      | <span data-ttu-id="bc260-189">Modification de la sélection actuelle dans le ListView.</span><span class="sxs-lookup"><span data-stu-id="bc260-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="bc260-190">Afficher les modifications</span><span class="sxs-lookup"><span data-stu-id="bc260-190">View Change</span></span>    | <span data-ttu-id="bc260-191">Modification de l’ordre de présentation ou du mode d’affichage dans ListView.</span><span class="sxs-lookup"><span data-stu-id="bc260-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
