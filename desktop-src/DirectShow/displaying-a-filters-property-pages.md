---
description: Affichage des pages de propriétés d’un filtre
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Affichage des pages de propriétés d’un filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999659"
---
# <a name="displaying-a-filters-property-pages"></a>Affichage des pages de propriétés d’un filtre

Une page de propriétés est un moyen pour un filtre de prendre en charge les propriétés que l’utilisateur peut définir. Cet article explique comment afficher les pages de propriétés d’un filtre dans une application. Pour plus d’informations sur les pages de propriétés, consultez la documentation du kit de développement Platform SDK.

> [!Note]  
> bien que la plupart des filtres fournis avec DirectShow prennent en charge les pages de propriétés, ils sont destinés à des fins de débogage et ne sont pas recommandés pour l’utilisation des applications. Dans la plupart des cas, les fonctionnalités équivalentes sont fournies par le biais d’une interface personnalisée sur le filtre. Une application doit contrôler ces filtres par programme, plutôt que d’exposer leurs pages de propriétés aux utilisateurs.

 

Les filtres avec les pages de propriétés exposent l’interface **ISpecifyPropertyPages** . Pour déterminer si un filtre définit une page de propriétés, interrogez le filtre pour cette interface à l’aide de **QueryInterface**.

Si vous avez créé directement une instance d’un filtre (en appelant **CoCreateInstance**), vous avez déjà un pointeur vers le filtre. Si ce n’est pas le cas, vous pouvez énumérer les filtres dans le graphique à l’aide de la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) . Pour plus d’informations, consultez [énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md).

Une fois que vous avez le pointeur d’interface **ISpecifyPropertyPages** , récupérez les pages de propriétés du filtre en appelant la méthode **ISpecifyPropertyPages :: GetPages** . Cette méthode remplit un tableau compté d’identificateurs globaux uniques (GUID) à l’aide de l’identificateur de classe (CLSID) de chaque page de propriétés. Un tableau compté est défini par une structure **cauuid** , que vous devez allouer, mais n’avez pas à initialiser. La méthode **GetPages** alloue le tableau, qui est contenu dans le membre **pElems** de la structure **cauuid** . Lorsque vous avez terminé, libérez le tableau en appelant la fonction **CoTaskMemFree** .

La fonction **OleCreatePropertyFrame** fournit un moyen simple d’afficher les pages de propriétés dans une boîte de dialogue modale.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[tâches de base DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



