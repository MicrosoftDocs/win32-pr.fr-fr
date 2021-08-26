---
description: Utilisation de DMOs dans DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Utilisation de DMOs dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078649"
---
# <a name="using-dmos-in-directshow"></a>Utilisation de DMOs dans DirectShow

les Applications basées sur DirectShow peuvent utiliser DMOs dans un graphique de filtre, par le biais du filtre de [Wrapper DMO](dmo-wrapper-filter.md) . ce filtre agrège une DMO et gère tous les détails de l’utilisation de l’DMO, comme le passage de données vers et depuis le DMO, l’allocation d’objets [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) , etc.

étant donné que le DMO est agrégé par le filtre, l’application peut interroger le filtre sur toutes les interfaces COM exposées par le DMO. Toutefois, l’application doit laisser le filtre gérer toutes les opérations de streaming sur le DMO. par exemple, ne définissez pas les types de média, traitez les mémoires tampons, videz le DMO, verrouillez le DMO, activez ou désactivez le contrôle de qualité, ou définissez des optimisations vidéo.

si vous connaissez l’identificateur de classe (CLSID) d’un DMO spécifique que vous souhaitez utiliser, vous pouvez initialiser le filtre de Wrapper DMO avec ce DMO, comme suit :

1.  appelez **CoCreateInstance** pour créer le filtre de Wrapper DMO.
2.  interrogez le filtre de Wrapper DMO pour l’interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Appelez la méthode [**IDMOWrapperFilter :: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . spécifiez le CLSID de la DMO et le GUID de la catégorie du DMO. pour obtenir la liste des catégories de DMO, consultez [DMO guid](dmo-guids.md).

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



La fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) énumère DMOs dans le registre. cette fonction utilise un autre jeu de guid de catégorie que ceux utilisés pour les filtres de DirectShow.

**Utilisation de l’énumérateur de périphérique système avec DMOs**

au lieu de créer directement un DMO, vous pouvez utiliser l' [énumérateur de périphérique système](system-device-enumerator.md), qui peut énumérer toute catégorie de DMO prise en charge par la méthode **DMOEnum** . l’énumérateur de périphérique système comprend également DMOs quand il énumère certains DirectShow des catégories de filtre. le tableau suivant montre le mappage entre les catégories de DMO et les catégories de DirectShow.



| Étiquette | Valeur |
|-----------------------------|--------------------------------|
| DMO Catégorie                | DirectShow Identique          |
| \_encodeur audio DMOCATEGORY \_ | CLSID \_ AudioCompressorCategory |
| \_DÉcodeur audio DMOCATEGORY \_ | CLSID \_ LegacyAmFilterCategory  |
| \_encodeur vidéo DMOCATEGORY \_ | CLSID \_ VideoCompressorCategory |
| \_DÉcodeur vidéo DMOCATEGORY \_ | CLSID \_ LegacyAmFilterCategory  |



 

L’énumérateur de périphérique système retourne une liste d’objets moniker. si le moniker représente un DMO, la méthode **IMoniker :: BindToObject** crée automatiquement le filtre de Wrapper DMO et l’initialise avec ce DMO. ainsi, le fait qu’une DMO est impliquée est transparent pour l’application. Pour plus d’informations sur l’utilisation de l’énumérateur de périphérique système, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

**Limitations**

Il existe certaines limitations lors de l’utilisation de DMOs dans DirectShow :

-   le filtre de Wrapper DMO ne prend pas en charge DMOs avec des entrées égales à zéro, plusieurs entrées ou des sorties nulles.
-   toutes les connexions de code confidentiel sur le filtre de Wrapper DMO utilisent l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   DirectShow les Services d’édition ne prennent pas en charge les effets ou transitions basés sur DMO.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DMOs](using-dmos.md)
</dt> </dl>

 

 



