---
description: Filtre de wrappers DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Filtre de wrappers DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b01ee006203e2e1fd328bacc13c01de4a3b25f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482433"
---
# <a name="dmo-wrapper-filter"></a>Filtre de wrappers DMO

Le filtre de wrapper DMO permet à une application DirectShow d’utiliser un [objet de média DirectX](directx-media-objects.md) (DMO) dans un graphique de filtre. Le filtre encapsule la requête DMO et gère tous les détails de l’utilisation d’DMO, tels que le transfert de données vers et depuis DMO. En outre, le filtre regroupe la fonction DMO, de sorte que l’application peut interroger le filtre sur toutes les interfaces COM exposées par le module DMO.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Types de média de broche d’entrée                    | Voir les notes                                                                                                                                                                                                                                        |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Types de média de broche de sortie                   | Voir les notes                                                                                                                                                                                                                                        |
| Interfaces de broche de sortie                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                                                                                                                   |
| Exécutable                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Mérite](merit.md)                       | Voir les notes                                                                                                                                                                                                                                        |
| [Catégorie de filtre](filter-categories.md) | Voir les notes                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Notes

### <a name="limitations"></a>Limites

Le wrapper DMO présente les limitations suivantes :

-   Il ne prend pas en charge DMOs avec des entrées égales à zéro, des entrées multiples ou des sorties nulles. (Elle prend en charge DMOs avec une entrée et plusieurs sorties.)
-   Il ne prend pas en charge les transports personnalisés. Tout le transport de données s’effectue par le biais de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Elle n’utilise pas l’interface **IMediaObjectInPlace** ; tout le traitement s’effectue à l’aide des méthodes [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Épingles

Pour chaque flux d’entrée sur DMO, le filtre crée une broche d’entrée correspondante. Pour chaque flux de sortie, il crée une broche de sortie correspondante. Les types de médias pris en charge par chaque pin dépendent de la

### <a name="encoder-interfaces"></a>Interfaces d’encodeur

Si DMO est un encodeur vidéo ou audio, la broche de sortie expose l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . Si DMO est un encodeur vidéo, la broche de sortie expose également l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Dans les deux cas, si la DMO prend en charge l’interface, le code PIN délègue à la DMO. Dans le cas contraire, le code PIN fournit sa propre implémentation.

### <a name="streaming"></a>Diffusion en continu

Le filtre utilise l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) pour gérer la diffusion en continu. Elle ne prend pas en charge les connexions [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Le filtre appelle [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) sur la solution DMO uniquement lorsqu’il reçoit des données à partir de en amont (y compris les notifications de fin de flux). Par conséquent, il ne prend pas en charge DMOs avec des flux d’entrée nuls.

### <a name="seeking"></a>Cherche

Toutes les demandes de recherche sont transmises au filtre amont, via la première broche d’entrée sur le wrapper DMO. Pour les DMOs à sortie multiple, cela signifie que le filtre en amont peut recevoir plusieurs demandes de recherche lorsque l’application recherche le graphique.

### <a name="merit"></a>Mérite

DirectShow affecte à tous les DMOs une valeur mérite par défaut de **mérite \_ normal** + 0x800. Cette valeur est comprise entre **mérite \_ normale** et **mérite \_ préféré**. Les filtres de décodeur ont généralement une valeur mérite de **mérite \_ normal**. Par conséquent, le gestionnaire de graphique de filtre sélectionne généralement un décodeur DMO sur un filtre de décodeur. Pour remplacer la valeur de mérite par défaut, ajoutez une entrée de Registre à la clé de Registre DMO dans HKEY \_ classes \_ racine \\ CLSID. Incluez une valeur **DWORD** nommée « mérite » dont la valeur spécifie le mérite.

### <a name="category"></a>Category

Le filtre de wrapper DMO n’apparaît pas en soi dans une catégorie. Lorsqu’il encapsule un objet DMO, il apparaît dans la catégorie DirectShow qui correspond à la catégorie DMO, sous le nom de la classe DMO.

### <a name="buffers"></a>Mémoires tampons

Le filtre de wrapper DMO transmet des tampons de média à la requête DMO qui expose l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

Dans Windows Vista ou version ultérieure, les mémoires tampons de média exposent également l’interface IServiceProvider. DMO peut utiliser cette interface pour obtenir un pointeur vers l’exemple de média associé à la mémoire tampon. Utilisez l’IID de l’identificateur de service **\_ IMediaSample**. Une vidéo DMO peut utiliser l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) de l’exemple de support pour définir des indicateurs d’entrelacement sur l’échantillon. Le code suivant illustre l’obtention du pointeur vers l’exemple de média :


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Pour plus d’informations sur les indicateurs entrelacés par exemple, consultez [**am \_ SAMPLE2 \_ Properties structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Contrôle qualité

Si la requête DMO expose l’interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , le filtre traduit les appels [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) sur sa broche de sortie en appels [**IDMOQUALITYCONTROL :: SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) sur DMO. Le paramètre *rtNow* de **SetNow** est calculé comme la somme de l' **horodateur** et des membres **tardifs** de la structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Utilisation de créateur dans GraphEdit

Dans GraphEdit, le filtre de wrappers DMO n’apparaît pas sous son propre nom. Au lieu de cela, chaque DMO inscrit est répertorié sous la catégorie de filtre appropriée. Lorsque vous ajoutez un module DMO via la boîte de dialogue **Insérer des filtres** , GraphEdit crée le filtre de wrapper DMO et le configure pour qu’il utilise ce DMO.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Objets multimédia DirectX](directx-media-objects.md)
</dt> </dl>

 

 
