---
description: Définissez les propriétés Allocator dans le cadre de l’écriture d’un filtre de transformation. La broche de sortie du filtre de transformation sélectionne l’allocateur en aval.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Étape 4. Définir les propriétés d’allocateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33376cff0e6c0674edfadcffed59d16d8d7dccb9f48384a22ec4c69fc48d8eb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652129"
---
# <a name="step-4-set-allocator-properties"></a>Étape 4. Définir les propriétés d’allocateur

Il s’agit de l’étape 4 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

> [!Note]  
> Cette étape n’est pas requise pour les filtres qui dérivent de **CTransInPlaceFilter**.

 

Une fois que deux codes PIN sont en accord sur un type de média, ils sélectionnent un allocateur pour la connexion et négocient les propriétés d’allocateur, telles que la taille de la mémoire tampon et le nombre de mémoires tampons.

Dans la classe **CTransformFilter** , il existe deux allocations : une pour la connexion de code confidentiel en amont et une pour la connexion de code confidentiel en aval. Le filtre amont sélectionne l’allocateur en amont et choisit également les propriétés Allocator. La broche d’entrée accepte tout ce que le filtre en amont décide. Si vous avez besoin de modifier ce comportement, remplacez la méthode [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .

La broche de sortie du filtre de transformation sélectionne l’allocateur en aval. Il permet d'effectuer les opérations suivantes :

1.  Si le filtre en aval peut fournir un allocateur, la broche de sortie utilise celle-ci. Dans le cas contraire, la broche de sortie crée un nouvel allocateur.
2.  La broche de sortie obtient les exigences d’allocateur du filtre en aval (le cas échéant) en appelant [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  La broche de sortie appelle la méthode [**CTransformFilter ::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) du filtre de transformation, qui est virtuelle pure. Les paramètres de cette méthode sont un pointeur vers l’allocateur et une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) avec les exigences du filtre en aval. Si le filtre en aval n’a pas de spécifications d’allocateur, la structure est mise à zéro.
4.  Dans la méthode **DecideBufferSize** , la classe dérivée définit les propriétés Allocator en appelant [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

En règle générale, la classe dérivée sélectionne des propriétés Allocator en fonction du format de sortie, des exigences du filtre en aval et des exigences propres au filtre. Essayez de sélectionner les propriétés qui sont compatibles avec la requête du filtre en aval. Dans le cas contraire, le filtre en aval risque de rejeter la connexion.

Dans l’exemple suivant, l’encodeur RLE définit des valeurs minimales pour la taille de la mémoire tampon, l’alignement de la mémoire tampon et le nombre de mémoires tampons. Pour le préfixe, elle utilise la valeur que le filtre en aval a demandée. Le préfixe est généralement de zéro octet, mais certains filtres l’exigent. Par exemple, le filtre [MUX AVI](avi-mux-filter.md) utilise le préfixe pour écrire des en-têtes riff.


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



L’allocateur peut ne pas être en mesure de correspondre exactement à votre demande. Par conséquent, la méthode **SetProperties** retourne le résultat réel dans une structure de **\_ propriétés d’allocateur** distincte (le paramètre *réel* , dans l’exemple précédent). Même lorsque **SetProperties** aboutit, vous devez vérifier le résultat pour vous assurer qu’ils répondent aux exigences minimales de votre filtre.

**Allocateurs personnalisés**

Par défaut, toutes les classes de filtre utilisent la classe [**CMemAllocator**](cmemallocator.md) pour leurs allocateurs. Cette classe alloue de la mémoire à partir de l’espace d’adressage virtuel du processus client (à l’aide de **VirtualAlloc**). Si votre filtre doit utiliser un autre type de mémoire, tel que des surfaces DirectDraw, vous pouvez implémenter un allocateur personnalisé. Vous pouvez utiliser la classe [**CBaseAllocator**](cbaseallocator.md) ou écrire une classe Allocator entièrement nouvelle. Si votre filtre a un allocateur personnalisé, substituez les méthodes suivantes, en fonction du code PIN utilisé par l’allocateur :

-   Broche d’entrée : [**CBaseInputPin :: GetAllocator**](cbaseinputpin-getallocator.md) et [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Broche de sortie : [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).

Si l’autre filtre refuse de se connecter à l’aide de votre allocateur personnalisé, votre filtre peut faire échouer la connexion ou se connecter avec l’allocateur d’un autre filtre. Dans ce dernier cas, vous devrez peut-être définir un indicateur interne indiquant le type d’allocateur. Pour obtenir un exemple de cette approche, consultez [**CDrawImage, classe**](cdrawimage.md).

Suivant : [étape 5. Transformez l’image](step-5--transform-the-image.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



