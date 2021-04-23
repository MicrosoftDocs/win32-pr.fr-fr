---
description: Utilisation de DMOs dans DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Utilisation de DMOs dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908687"
---
# <a name="using-dmos-in-directshow"></a>Utilisation de DMOs dans DirectShow

Les applications basées sur DirectShow peuvent utiliser DMOs dans un graphique de filtre, par le biais du filtre de [wrappers DMO](dmo-wrapper-filter.md) . Ce filtre agrège un DMO et gère tous les détails de l’utilisation d’DMO, tels que le transfert de données vers et à partir d’DMO, l’allocation d’objets [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) , etc.

Dans la mesure où DMO est agrégé par le filtre, l’application peut interroger le filtre sur toutes les interfaces COM exposées par DMO. Toutefois, l’application doit laisser le filtre gérer toutes les opérations de diffusion en continu sur DMO. Par exemple, ne définissez pas les types de média, traitez les mémoires tampons, videz le système DMO, verrouillez DMO, activez ou désactivez le contrôle qualité, ou définissez des optimisations vidéo.

Si vous connaissez l’identificateur de classe (CLSID) d’un DMO spécifique que vous souhaitez utiliser, vous pouvez initialiser le filtre de wrappers DMO avec ce DMO, comme suit :

1.  Appelez **CoCreateInstance** pour créer le filtre de wrappers DMO.
2.  Interrogez le filtre de wrappers DMO pour l’interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Appelez la méthode [**IDMOWrapperFilter :: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . Spécifiez le CLSID de la classe DMO et le GUID de la catégorie DMO. Pour obtenir la liste des catégories DMO, consultez [GUID DMO](dmo-guids.md).

Le code suivant illustre ces étapes :


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



La fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) énumère DMOs dans le registre. Cette fonction utilise un autre jeu de GUID de catégorie que ceux utilisés pour les filtres DirectShow.

**Utilisation de l’énumérateur de périphérique système avec DMOs**

Au lieu de créer directement un DMO, vous pouvez utiliser l' [énumérateur de périphérique système](system-device-enumerator.md), qui peut énumérer toute catégorie DMO prise en charge par la méthode **DMOEnum** . L’énumérateur de périphérique système comprend également DMOs lorsqu’il énumère certaines catégories de filtre DirectShow. Le tableau suivant montre le mappage entre les catégories DMO et les catégories DirectShow.



| Étiquette | Valeur |
|-----------------------------|--------------------------------|
| Catégorie DMO                | Équivalent DirectShow          |
| \_encodeur audio DMOCATEGORY \_ | CLSID \_ AudioCompressorCategory |
| \_DÉcodeur audio DMOCATEGORY \_ | CLSID \_ LegacyAmFilterCategory  |
| \_encodeur vidéo DMOCATEGORY \_ | CLSID \_ VideoCompressorCategory |
| \_DÉcodeur vidéo DMOCATEGORY \_ | CLSID \_ LegacyAmFilterCategory  |



 

L’énumérateur de périphérique système retourne une liste d’objets moniker. Si le moniker représente un DMO, la méthode **IMoniker :: BindToObject** crée automatiquement le filtre de wrappers DMO et l’initialise avec ce DMO. Ainsi, le fait qu’un DMO soit impliqué est transparent pour l’application. Pour plus d’informations sur l’utilisation de l’énumérateur de périphérique système, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

**Limitations**

Il existe certaines limitations lors de l’utilisation de DMOs dans DirectShow :

-   Le filtre de wrapper DMO ne prend pas en charge DMOs avec des entrées égales à zéro, plusieurs entrées ou des sorties nulles.
-   Toutes les connexions de code confidentiel sur le filtre de wrapper DMO utilisent l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Les services d’édition DirectShow ne prennent pas en charge les effets ou transitions basés sur DMO.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DMOs](using-dmos.md)
</dt> </dl>

 

 



