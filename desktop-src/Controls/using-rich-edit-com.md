---
title: Utilisation d’OLE dans des contrôles RichEdit
description: Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115265"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a>Utilisation d’OLE dans des contrôles RichEdit

Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-interface"></a>Utiliser une interface de modification enrichie

Les contrôles RichEdit exposent certaines de leurs fonctionnalités via des interfaces COM (Component Object Model). En obtenant une interface à partir d’un contrôle, vous avez la possibilité d’utiliser d’autres objets dans le contrôle. Vous pouvez obtenir cette interface en envoyant le message [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) . À partir de l’interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) , vous pouvez obtenir des interfaces utilisées dans le [modèle d’objet de texte](text-object-model.md).

Une autre interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), est implémentée par les applications pour définir le comportement du contrôle lorsqu’il interagit avec les objets.

### <a name="insert-an-object-into-a-rich-edit-control"></a>Insérer un objet dans un contrôle RichEdit

L’exemple de code suivant insère un objet fichier dans un contrôle RichEdit. si un programme est associé au type de fichier sur l’ordinateur de l’utilisateur (par exemple, Microsoft Excel pour un fichier .xls), le contenu du fichier s’affiche dans le contrôle ; dans le cas contraire, une icône s’affiche.

1.  Obtient l’interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) .

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  Créez un stockage structuré.

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  Configurez le format de données.

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  Obtient un pointeur vers le site d’affichage.

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  Créez l’objet et récupérez son interface **IUnknown** .

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

    

6.  Obtient l’interface IOleObject pour l’objet.

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  Pour vous assurer que les références sont correctement comptées, avertissez l’objet qu’il contient.

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  Configurez les informations de l’objet.

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

    

9.  Placer le signe insertion à la fin du texte et ajouter un retour chariot.

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. Insérez l’objet.

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. Nettoyer.

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a>Utilisation de IRichEditOleCallback

Les applications implémentent l’interface [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) pour répondre à des requêtes ou des actions liées à OLE qui sont effectuées par un contrôle RichEdit. Vous associez votre implémentation de l’interface au contrôle en envoyant un message [**em \_ SETOLECALLBACK**](em-setolecallback.md) . Le contrôle appelle ensuite des méthodes sur votre implémentation de l’interface, le cas échéant.

Par exemple, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) est appelé quand l’utilisateur tente de faire glisser ou de coller un objet dans le contrôle. Si votre application peut accepter les données, votre implémentation de la méthode retourne S \_ OK ; sinon, elle retourne un code d’erreur. La méthode peut également prendre une autre action, par exemple avertir l’utilisateur que les fichiers de ce type ne peuvent pas être placés dans le contrôle.

## <a name="complete-insertobject-example-function"></a>Remplir l’exemple de fonction InsertObject

L’exemple de code suivant montre les extraits de code précédents combinés dans une fonction complète qui comprend la gestion des erreurs.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




