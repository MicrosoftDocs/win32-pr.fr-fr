---
title: Utilisation d’OLE dans des contrôles RichEdit
description: Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101380"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="39b42-103">Utilisation d’OLE dans des contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="39b42-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="39b42-104">Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit.</span><span class="sxs-lookup"><span data-stu-id="39b42-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="39b42-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="39b42-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="39b42-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="39b42-106">Technologies</span></span>

-   [<span data-ttu-id="39b42-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="39b42-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="39b42-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="39b42-108">Prerequisites</span></span>

-   <span data-ttu-id="39b42-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="39b42-109">C/C++</span></span>
-   <span data-ttu-id="39b42-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="39b42-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="39b42-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="39b42-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="39b42-112">Utiliser une interface de modification enrichie</span><span class="sxs-lookup"><span data-stu-id="39b42-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="39b42-113">Les contrôles RichEdit exposent certaines de leurs fonctionnalités via des interfaces COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="39b42-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="39b42-114">En obtenant une interface à partir d’un contrôle, vous avez la possibilité d’utiliser d’autres objets dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="39b42-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="39b42-115">Vous pouvez obtenir cette interface en envoyant le message [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="39b42-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="39b42-116">À partir de l’interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) , vous pouvez obtenir des interfaces utilisées dans le [modèle d’objet de texte](text-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="39b42-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="39b42-117">Une autre interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), est implémentée par les applications pour définir le comportement du contrôle lorsqu’il interagit avec les objets.</span><span class="sxs-lookup"><span data-stu-id="39b42-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="39b42-118">Insérer un objet dans un contrôle RichEdit</span><span class="sxs-lookup"><span data-stu-id="39b42-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="39b42-119">L’exemple de code suivant insère un objet fichier dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="39b42-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="39b42-120">Si un programme est associé au type de fichier sur l’ordinateur de l’utilisateur (par exemple, Microsoft Excel pour un fichier. xls), le contenu du fichier s’affiche dans le contrôle ; dans le cas contraire, une icône s’affiche.</span><span class="sxs-lookup"><span data-stu-id="39b42-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="39b42-121">Obtient l’interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="39b42-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="39b42-122">Créez un stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="39b42-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="39b42-123">Configurez le format de données.</span><span class="sxs-lookup"><span data-stu-id="39b42-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="39b42-124">Obtient un pointeur vers le site d’affichage.</span><span class="sxs-lookup"><span data-stu-id="39b42-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="39b42-125">Créez l’objet et récupérez son interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="39b42-125">Create the object and retrieve its **IUnknown** interface.</span></span>

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  <span data-ttu-id="39b42-126">Obtient l’interface IOleObject pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="39b42-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="39b42-127">Pour vous assurer que les références sont correctement comptées, avertissez l’objet qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="39b42-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="39b42-128">Configurez les informations de l’objet.</span><span class="sxs-lookup"><span data-stu-id="39b42-128">Set up object info.</span></span>

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  <span data-ttu-id="39b42-129">Placer le signe insertion à la fin du texte et ajouter un retour chariot.</span><span class="sxs-lookup"><span data-stu-id="39b42-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="39b42-130">Insérez l’objet.</span><span class="sxs-lookup"><span data-stu-id="39b42-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="39b42-131">Nettoyer.</span><span class="sxs-lookup"><span data-stu-id="39b42-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="39b42-132">Utilisation de IRichEditOleCallback</span><span class="sxs-lookup"><span data-stu-id="39b42-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="39b42-133">Les applications implémentent l’interface [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) pour répondre à des requêtes ou des actions liées à OLE qui sont effectuées par un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="39b42-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="39b42-134">Vous associez votre implémentation de l’interface au contrôle en envoyant un message [**em \_ SETOLECALLBACK**](em-setolecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="39b42-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="39b42-135">Le contrôle appelle ensuite des méthodes sur votre implémentation de l’interface, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="39b42-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="39b42-136">Par exemple, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) est appelé quand l’utilisateur tente de faire glisser ou de coller un objet dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="39b42-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="39b42-137">Si votre application peut accepter les données, votre implémentation de la méthode retourne S \_ OK ; sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="39b42-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="39b42-138">La méthode peut également prendre une autre action, par exemple avertir l’utilisateur que les fichiers de ce type ne peuvent pas être placés dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="39b42-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="39b42-139">Remplir l’exemple de fonction InsertObject</span><span class="sxs-lookup"><span data-stu-id="39b42-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="39b42-140">L’exemple de code suivant montre les extraits de code précédents combinés dans une fonction complète qui comprend la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="39b42-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="39b42-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39b42-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39b42-142">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="39b42-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="39b42-143">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="39b42-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




