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
# <a name="developing-with-windows-explorer"></a>Développement avec l’Explorateur Windows

L’Explorateur Windows est une application puissante de navigation et de gestion des ressources. L’Explorateur Windows est accessible en tant qu’ensemble intégré à Explorer.exe ou à l’interface [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . L’Explorateur Windows (Explorer.exe) peut être généré en tant que processus distinct à l’aide de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ou d’une fonction similaire.

> [!Note]  
> Les options de ligne de commande pour Explorer.exe sont documentées sur le site du support technique de Microsoft Windows dans l’article options d' Command-Line de l' [Explorateur Windows](https://support.microsoft.com/kb/152457).

 

Les fenêtres d’explorateur ouvertes peuvent être découvertes et programmées à l’aide de [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows), et de nouvelles instances de l’Explorateur Windows peuvent être créées à l’aide de [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

L’exemple de code suivant montre comment le modèle Automation de l’Explorateur Windows peut être utilisé pour créer et découvrir des fenêtres Explorateur qui exécutent.


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



La zone cliente de l’Explorateur Windows peut être hébergée à l’aide de l’interface [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Le client de l’Explorateur Windows et les contrôles d’arborescence de l’espace de noms sont des composants standard de Windows Vista et versions ultérieures. Les développeurs peuvent réutiliser les interfaces comme des composants de génération. Ces contrôles sont couramment utilisés pour créer des explorateurs personnalisés appropriés au domaine du problème.

Les contrôles de l’Explorateur Windows sont classés dans les catégories fonctionnelles suivantes :

-   [Contrôles de navigation](#navigation-controls)
-   [Contrôles de commande](#command-controls)
-   [Contrôles de propriété et d’aperçu](#property-and-preview-controls)
-   [Filtrage et affichage des contrôles](#filtering-and-view-controls)
-   [Contrôle ListView](#listview-control)

## <a name="navigation-controls"></a>Contrôles de navigation

Les contrôles de navigation aident les utilisateurs à déterminer le contexte et à naviguer dans l’espace de domaine logique associé, appelé espace. Par exemple, le espace pour l’Explorateur Windows est l’espace de noms Shell. Les espaces sont composés de zéro ou de plusieurs pages.

Le tableau suivant répertorie et décrit les contrôles de navigation disponibles dans l’Explorateur Windows dans les systèmes d’exploitation Windows Vista et versions ultérieures.



| Contrôle de navigation               | Description                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barre d’adresses (contrôle de navigation) | Affiche l’adresse de la page actuelle dans le espace. Vous pouvez cliquer sur les boutons de navigation pour accéder à n’importe quel ancêtre dans le espace. Les utilisateurs peuvent également taper des URL et des chemins d’accès pour naviguer. |
| Arborescence des dossiers                      | Fournit une nouvelle version d’un contrôle d’arborescence, optimisé pour les grands espaces.                                                                                                                  |
| Voyage                           | Active la navigation relative par le biais de boutons de style Web tels que **précédent** et **suivant**.                                                                                                    |
| Intitulé                            | Affiche le nom et le contexte de l’Explorateur actuel.                                                                                                                                            |
| Espace                        | Affiche la branche active de la espace. Les pages peuvent être classées selon différents critères. Les utilisateurs peuvent cliquer sur une page pour y accéder.                                                        |



 

## <a name="command-controls"></a>Contrôles de commande

Les contrôles de commande publient les fonctionnalités de l’Explorateur Windows pour les utilisateurs. Ces contrôles effectuent des actions générales ou des actions spécifiques à un ou plusieurs éléments sélectionnés.



| Contrôle de commande | Description                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barre d’outils         | Affiche des boutons pour les commandes couramment utilisées (une nouvelle version d’une barre d’outils de commande). Les options de personnalisation incluent des boutons déroulants, des boutons partagés, du texte descriptif facultatif et une zone de dépassement. |
| Bannière            | S’affiche sous la forme d’un contrôle personnalisé unique, facultatif, au centre de la barre d’outils. Il représente la commande principale pour le contexte actuel.                                                             |
| Barre de menus        | Présente les commandes dans les menus.                                                                                                                                                                   |
| Menu contextuel    | Répertorie un sous-ensemble approprié des commandes disponibles, qui s’affichent à la suite d’un clic droit sur un élément.                                                                               |



 

## <a name="property-and-preview-controls"></a>Contrôles de propriété et d’aperçu

Les contrôles de propriété et d’aperçu permettent d’afficher un aperçu des éléments, ainsi que d’afficher et de modifier les propriétés d’un élément.



| Control    | Description                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRÉVERSION    | Affiche un aperçu de l’élément sélectionné, tel qu’une miniature ou une icône en direct.                                                                                                                                                                       |
| Propriétés | Affiche les propriétés de l’élément sélectionné. Pour les sélections multiples, elle affiche un résumé des propriétés pour le groupe d’éléments sélectionné. Pour une sélection null, elle affiche un résumé des propriétés de la page actuelle (contenu de ListView). |



 

## <a name="filtering-and-view-controls"></a>Filtrage et affichage des contrôles

Les contrôles de filtrage et d’affichage permettent de manipuler l’ensemble des éléments de ListView et de modifier la présentation des éléments dans ListView.



| Control   | Description                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtrer    | Filtre ou organise des éléments dans un ListView en fonction des propriétés listées en tant que colonnes. Cliquer sur une colonne trie par cette propriété. |
| Wordwheel | Filtre de façon dynamique et incrémentielle les éléments affichés dans un ListView en fonction d’une chaîne de texte d’entrée.                      |
| Affichage      | Permet à l’utilisateur de modifier le mode d’affichage d’un contrôle ListView. Un curseur peut être utilisé pour déterminer la taille des icônes.                |



 

## <a name="listview-control"></a>Contrôle ListView

Le contrôle ListView est utilisé pour afficher un ensemble d’éléments dans l’un des quatre modes d’affichage suivants : détails, vignettes, icônes ou Panorama. Le contrôle ListView permet également à l’utilisateur de sélectionner et d’activer un ou plusieurs éléments.

> [!Caution]  
> Bien que certains de ces contrôles aient des noms et/ou des fonctionnalités qui sont similaires aux contrôles de Windows Presentation Foundation standard (WPF) présents dans l’espace de noms System. Windows. Controls, il s’agit de classes distinctes.

 

Ces contrôles distincts fonctionnent ensemble en grande partie par le biais d’événements générés par l’interaction de l’utilisateur ou par les contrôles eux-mêmes. Le tableau suivant présente les trois principales catégories d’événements.



| Catégorie d'événements | Exemple                                                       |
|----------------|---------------------------------------------------------------|
| Navigation     | Passage d’une page à l’autre.                               |
| Sélection      | Modification de la sélection actuelle dans le ListView.               |
| Afficher les modifications    | Modification de l’ordre de présentation ou du mode d’affichage dans ListView. |



 

 

 
