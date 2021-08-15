---
description: Windows L’Explorateur est une application puissante de navigation et de gestion des ressources.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: développement avec l’explorateur de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d00b513b3ee73c30b100cb4236d2c9fb327e1f9557d12ba86738ee9e910ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460182"
---
# <a name="developing-with-windows-explorer"></a>développement avec l’explorateur de Windows

Windows L’Explorateur est une application puissante de navigation et de gestion des ressources. Windows L’Explorateur est accessible en tant qu’ensemble intégré via Explorer.exe ou l’interface [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Windows L’Explorateur (Explorer.exe) peut être généré en tant que processus distinct à l’aide de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou d’une fonction similaire.

> [!Note]  
> les options de ligne de commande pour Explorer.exe sont documentées sur le site du Support technique Microsoft Windows dans l’article [options de Command-Line de Windows Explorer](https://support.microsoft.com/kb/152457).

 

les fenêtres d’explorateur ouvertes peuvent être découvertes et programmées à l’aide de [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (clsid \_ ShellWindows), et de nouvelles instances de Windows explorer peuvent être créées à l’aide de [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (clsid \_ ShellBrowserWindow).

l’exemple de code suivant montre comment le modèle automation Windows explorer peut être utilisé pour créer et découvrir des fenêtres explorateur qui exécutent.


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



la zone cliente Windows Explorer peut être hébergée à l’aide de l’interface [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . le client Windows Explorer et les contrôles d’arborescence d’espace de noms sont des composants standard de Windows Vista et versions ultérieures. Les développeurs peuvent réutiliser les interfaces comme des composants de génération. Ces contrôles sont couramment utilisés pour créer des explorateurs personnalisés appropriés au domaine du problème.

les contrôles de Windows Explorer sont classés dans les catégories fonctionnelles suivantes :

-   [Contrôles de navigation](#navigation-controls)
-   [Contrôles de commande](#command-controls)
-   [Contrôles de propriété et d’aperçu](#property-and-preview-controls)
-   [Filtrage et affichage des contrôles](#filtering-and-view-controls)
-   [Contrôle ListView](#listview-control)

## <a name="navigation-controls"></a>Contrôles de navigation

Les contrôles de navigation aident les utilisateurs à déterminer le contexte et à naviguer dans l’espace de domaine logique associé, appelé espace. par exemple, le espace pour Windows Explorer est l’espace de noms Shell. Les espaces sont composés de zéro ou de plusieurs pages.

le tableau suivant répertorie et décrit les contrôles de navigation disponibles dans Windows Explorer dans les systèmes d’exploitation Windows Vista et versions ultérieures.



| Contrôle de navigation               | Description                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barre d’adresses (contrôle de navigation) | Affiche l’adresse de la page actuelle dans le espace. Vous pouvez cliquer sur les boutons de navigation pour accéder à n’importe quel ancêtre dans le espace. Les utilisateurs peuvent également taper des URL et des chemins d’accès pour naviguer. |
| Arborescence des dossiers                      | Fournit une nouvelle version d’un contrôle d’arborescence, optimisé pour les grands espaces.                                                                                                                  |
| Voyage                           | Active la navigation relative par le biais de boutons de style Web tels que **précédent** et **suivant**.                                                                                                    |
| Titre                            | Affiche le nom et le contexte de l’Explorateur actuel.                                                                                                                                            |
| Espace                        | Affiche la branche active de la espace. Les pages peuvent être classées selon différents critères. Les utilisateurs peuvent cliquer sur une page pour y accéder.                                                        |



 

## <a name="command-controls"></a>Contrôles de commande

les contrôles de commande publient les fonctionnalités de l’explorateur de Windows pour les utilisateurs. Ces contrôles effectuent des actions générales ou des actions spécifiques à un ou plusieurs éléments sélectionnés.



| Contrôle de commande | Description                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barre d’outils         | Affiche des boutons pour les commandes couramment utilisées (une nouvelle version d’une barre d’outils de commande). Les options de personnalisation incluent des boutons déroulants, des boutons partagés, du texte descriptif facultatif et une zone de dépassement. |
| Bannière            | S’affiche sous la forme d’un contrôle personnalisé unique, facultatif, au centre de la barre d’outils. Il représente la commande principale pour le contexte actuel.                                                             |
| Barre de menus        | Présente les commandes dans les menus.                                                                                                                                                                   |
| Menu contextuel    | Répertorie un sous-ensemble approprié des commandes disponibles, qui s’affichent à la suite d’un clic droit sur un élément.                                                                               |



 

## <a name="property-and-preview-controls"></a>Contrôles de propriété et d’aperçu

Les contrôles de propriété et d’aperçu permettent d’afficher un aperçu des éléments, ainsi que d’afficher et de modifier les propriétés d’un élément.



| Contrôler    | Description                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Préversion    | Affiche un aperçu de l’élément sélectionné, tel qu’une miniature ou une icône en direct.                                                                                                                                                                       |
| Propriétés | Affiche les propriétés de l’élément sélectionné. Pour les sélections multiples, elle affiche un résumé des propriétés pour le groupe d’éléments sélectionné. Pour une sélection null, elle affiche un résumé des propriétés de la page actuelle (contenu de ListView). |



 

## <a name="filtering-and-view-controls"></a>Filtrage et affichage des contrôles

Les contrôles de filtrage et d’affichage permettent de manipuler l’ensemble des éléments de ListView et de modifier la présentation des éléments dans ListView.



| Contrôler   | Description                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtrer    | Filtre ou organise des éléments dans un ListView en fonction des propriétés listées en tant que colonnes. Cliquer sur une colonne trie par cette propriété. |
| Wordwheel | Filtre de façon dynamique et incrémentielle les éléments affichés dans un ListView en fonction d’une chaîne de texte d’entrée.                      |
| Affichage      | Permet à l’utilisateur de modifier le mode d’affichage d’un contrôle ListView. Un curseur peut être utilisé pour déterminer la taille des icônes.                |



 

## <a name="listview-control"></a>Contrôle ListView

Le contrôle ListView est utilisé pour afficher un ensemble d’éléments dans l’un des quatre modes d’affichage suivants : détails, vignettes, icônes ou Panorama. Le contrôle ListView permet également à l’utilisateur de sélectionner et d’activer un ou plusieurs éléments.

> [!Caution]  
> bien que certains de ces contrôles aient des noms et/ou des fonctionnalités qui sont semblables aux contrôles de Windows Presentation Foundation standard (WPF) présents dans le système. Windows. Contrôle l’espace de noms, il s’agit de classes distinctes.

 

Ces contrôles distincts fonctionnent ensemble en grande partie par le biais d’événements générés par l’interaction de l’utilisateur ou par les contrôles eux-mêmes. Le tableau suivant présente les trois principales catégories d’événements.



| Catégorie d'événements |  Exemple                                                       |
|----------------|---------------------------------------------------------------|
| Navigation     | Passage d’une page à l’autre.                               |
| Sélection      | Modification de la sélection actuelle dans le ListView.               |
| Afficher les modifications    | Modification de l’ordre de présentation ou du mode d’affichage dans ListView. |



 

 

 
