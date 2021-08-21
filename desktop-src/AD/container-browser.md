---
title: Navigateur de conteneurs
description: Une application peut utiliser la fonction DsBrowseForContainer pour afficher une boîte de dialogue qui peut être utilisée pour parcourir les conteneurs dans un service domaine Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- PUBLICITÉ du navigateur de conteneurs
- conteneurs, navigateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd32cd7c172f08cd407feec50823fe410be4d13a36f4f0ee9ed1b2e75f11346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021939"
---
# <a name="container-browser"></a>Navigateur de conteneurs

Une application peut utiliser la fonction [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) pour afficher une boîte de dialogue qui peut être utilisée pour parcourir les conteneurs dans un service domaine Active Directory. La boîte de dialogue affiche les conteneurs dans un format d’arborescence et permet à l’utilisateur de parcourir l’arborescence à l’aide du clavier et de la souris. Lorsque l’utilisateur sélectionne un élément dans la boîte de dialogue, l’ADsPath du conteneur sélectionné par l’utilisateur est fourni.

[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) prend un pointeur vers une structure [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) qui contient les données relatives à la boîte de dialogue et retourne l’ADsPath de l’élément sélectionné.

Le membre **pszRoot** est un pointeur vers une chaîne Unicode qui contient le conteneur racine de l’arborescence. Si **pszRoot** a la **valeur null**, l’arborescence contiendra la totalité de l’arborescence.

Le membre **pszPath** reçoit l’ADsPath de l’objet sélectionné. Il est possible de spécifier un conteneur particulier à afficher et à sélectionner lorsque la boîte de dialogue s’affiche pour la première fois. Pour ce faire, définissez **pszPath** sur l’ADsPath de l’élément à sélectionner et définissez l’indicateur **DSBI \_ EXPANDONOPEN** dans **dwFlags**.

Le contenu et le comportement de la boîte de dialogue peuvent également être contrôlés au moment de l’exécution en implémentant une fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . La fonction **BFFCallBack** est implémentée par l’application et est appelée lorsque certains événements se produisent. Une application peut utiliser ces événements pour contrôler l’affichage des éléments de la boîte de dialogue, ainsi que le contenu réel de la boîte de dialogue. Par exemple, une application peut filtrer les éléments affichés dans la boîte de dialogue en implémentant une fonction **BFFCallBack** qui peut gérer la notification **DSBM \_ QUERYINSERT** . Quand une notification **DSBM \_ QUERYINSERT** est reçue, utilisez le membre **PszADsPath** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) pour déterminer quel élément est sur le point d’être inséré. Si l’application détermine que l’élément ne doit pas être affiché, elle peut masquer l’élément en effectuant les étapes suivantes.

1.  Ajoutez l’indicateur d' **\_ État DSBF** au membre **DwMask** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
2.  Ajoutez l’indicateur **DSBS \_ Hidden** au membre **DwStateMask** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
3.  Ajoutez l’indicateur **DSBS \_ Hidden** au membre **DwState** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .
4.  Retourne une valeur différente de zéro à partir de la fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .

En plus de masquer certains éléments, une application peut modifier le texte et l’icône affichés pour l’élément en gérant la notification **DSBM \_ QUERYINSERT** . Pour plus d’informations, consultez [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).

La fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) peut utiliser la **notification \_ initialisée par BFFM** pour obtenir le handle de la boîte de dialogue. L’application peut utiliser ce handle pour envoyer des messages, tels que **BFFM \_ ENABLEOK**, à la boîte de dialogue. Pour plus d’informations sur les messages qui peuvent être envoyés à la boîte de dialogue, consultez [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).

Le handle de la boîte de dialogue peut également être utilisé pour accéder directement aux contrôles de la boîte de dialogue. **DSBID \_ BANNER** est l’identificateur du contrôle de texte statique dans lequel le membre **pszTitle** de la structure [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) est affiché. **DSBID \_ CONTAINERLIST** est l’identificateur du contrôle TreeView utilisé pour afficher le contenu de l’arborescence. L’utilisation de ces éléments doit être évitée, si possible, pour éviter de futurs problèmes de compatibilité des applications.

L’exemple de code C++ suivant montre comment utiliser la fonction [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) pour créer la boîte de dialogue du navigateur de conteneurs et implémenter une fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) . [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) utilise la notification **DSBM \_ QUERYINSERT** pour remplacer le nom complet de chaque élément par le nom unique de l’élément.


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 