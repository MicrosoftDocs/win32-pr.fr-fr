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
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031040"
---
# <a name="container-browser"></a><span data-ttu-id="1a3a6-105">Navigateur de conteneurs</span><span class="sxs-lookup"><span data-stu-id="1a3a6-105">Container Browser</span></span>

<span data-ttu-id="1a3a6-106">Une application peut utiliser la fonction [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) pour afficher une boîte de dialogue qui peut être utilisée pour parcourir les conteneurs dans un service domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="1a3a6-107">La boîte de dialogue affiche les conteneurs dans un format d’arborescence et permet à l’utilisateur de parcourir l’arborescence à l’aide du clavier et de la souris.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="1a3a6-108">Lorsque l’utilisateur sélectionne un élément dans la boîte de dialogue, l’ADsPath du conteneur sélectionné par l’utilisateur est fourni.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="1a3a6-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) prend un pointeur vers une structure [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) qui contient les données relatives à la boîte de dialogue et retourne l’ADsPath de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="1a3a6-110">Le membre **pszRoot** est un pointeur vers une chaîne Unicode qui contient le conteneur racine de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="1a3a6-111">Si **pszRoot** a la **valeur null**, l’arborescence contiendra la totalité de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="1a3a6-112">Le membre **pszPath** reçoit l’ADsPath de l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="1a3a6-113">Il est possible de spécifier un conteneur particulier à afficher et à sélectionner lorsque la boîte de dialogue s’affiche pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="1a3a6-114">Pour ce faire, définissez **pszPath** sur l’ADsPath de l’élément à sélectionner et définissez l’indicateur **DSBI \_ EXPANDONOPEN** dans **dwFlags**.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="1a3a6-115">Le contenu et le comportement de la boîte de dialogue peuvent également être contrôlés au moment de l’exécution en implémentant une fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="1a3a6-116">La fonction **BFFCallBack** est implémentée par l’application et est appelée lorsque certains événements se produisent.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="1a3a6-117">Une application peut utiliser ces événements pour contrôler l’affichage des éléments de la boîte de dialogue, ainsi que le contenu réel de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="1a3a6-118">Par exemple, une application peut filtrer les éléments affichés dans la boîte de dialogue en implémentant une fonction **BFFCallBack** qui peut gérer la notification **DSBM \_ QUERYINSERT** .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="1a3a6-119">Quand une notification **DSBM \_ QUERYINSERT** est reçue, utilisez le membre **PszADsPath** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) pour déterminer quel élément est sur le point d’être inséré.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="1a3a6-120">Si l’application détermine que l’élément ne doit pas être affiché, elle peut masquer l’élément en effectuant les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="1a3a6-121">Ajoutez l’indicateur d' **\_ État DSBF** au membre **DwMask** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="1a3a6-122">Ajoutez l’indicateur **DSBS \_ Hidden** au membre **DwStateMask** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="1a3a6-123">Ajoutez l’indicateur **DSBS \_ Hidden** au membre **DwState** de la structure [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="1a3a6-124">Retourne une valeur différente de zéro à partir de la fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="1a3a6-125">En plus de masquer certains éléments, une application peut modifier le texte et l’icône affichés pour l’élément en gérant la notification **DSBM \_ QUERYINSERT** .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="1a3a6-126">Pour plus d’informations, consultez [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="1a3a6-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="1a3a6-127">La fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) peut utiliser la **notification \_ initialisée par BFFM** pour obtenir le handle de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="1a3a6-128">L’application peut utiliser ce handle pour envoyer des messages, tels que **BFFM \_ ENABLEOK**, à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="1a3a6-129">Pour plus d’informations sur les messages qui peuvent être envoyés à la boîte de dialogue, consultez [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="1a3a6-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="1a3a6-130">Le handle de la boîte de dialogue peut également être utilisé pour accéder directement aux contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="1a3a6-131">**DSBID \_ BANNER** est l’identificateur du contrôle de texte statique dans lequel le membre **pszTitle** de la structure [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) est affiché.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="1a3a6-132">**DSBID \_ CONTAINERLIST** est l’identificateur du contrôle TreeView utilisé pour afficher le contenu de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="1a3a6-133">L’utilisation de ces éléments doit être évitée, si possible, pour éviter de futurs problèmes de compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="1a3a6-134">L’exemple de code C++ suivant montre comment utiliser la fonction [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) pour créer la boîte de dialogue du navigateur de conteneurs et implémenter une fonction [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="1a3a6-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="1a3a6-135">[**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) utilise la notification **DSBM \_ QUERYINSERT** pour remplacer le nom complet de chaque élément par le nom unique de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1a3a6-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


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



 

 