---
description: Création de graphiques à l’aide du générateur de graphiques de capture
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Création de graphiques à l’aide du générateur de graphiques de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846729"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Création de graphiques à l’aide du générateur de graphiques de capture

En dépit de son nom, le générateur de graphiques de capture est utile pour créer de nombreux types de graphiques de filtres personnalisés, non seulement des graphiques de capture. Cet article fournit une brève vue d’ensemble de l’utilisation de cet objet.

Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Commencez par appeler [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le générateur de graphiques de capture et le gestionnaire de graphes de filtre. Ensuite, initialisez le générateur de graphiques de capture en appelant [**ICaptureGraphBuilder2 :: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) avec un pointeur vers le gestionnaire de graphique de filtre, comme suit :


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Connexion de filtres

La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) connecte deux ou trois filtres ensemble dans une chaîne. En règle générale, la méthode fonctionne mieux lorsque chaque filtre n’a pas plus d’une broche d’entrée ou d’une broche de sortie du même type. Pour commencer, cette discussion ignore les deux premiers paramètres de **RenderStream** et se focalise sur les trois derniers paramètres. Le troisième paramètre est un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , qui peut spécifier soit un filtre (comme pointeur d’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ), soit une broche de sortie (comme pointeur d’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) ). Les quatrième et cinquième paramètres spécifient des pointeurs **IBaseFilter** . La méthode **RenderStream** connecte les trois filtres dans une chaîne. Par exemple, supposons que *A*, *B* et *C* sont des filtres. Supposons que chaque filtre possède exactement une broche d’entrée et une broche de sortie. L’appel suivant connecte A à B, puis B à C :

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Toutes les connexions sont « intelligentes », ce qui signifie que des filtres supplémentaires sont ajoutés au graphique en fonction des besoins. Pour plus d’informations, consultez [connexion intelligente](intelligent-connect.md). Pour connecter uniquement deux filtres, définissez la valeur du milieu sur **null**. Par exemple, cet appel connecte un à C :

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Vous pouvez créer des chaînes plus longues en appelant la méthode à deux reprises :

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Si le dernier paramètre a la **valeur null**, la méthode localise automatiquement un convertisseur par défaut. Elle utilise le [convertisseur vidéo](video-renderer-filter.md) pour la vidéo et le [convertisseur DirectSound](directsound-renderer-filter.md) pour l’audio. Faisant

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

équivaut à :

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

où *R* est le convertisseur approprié. Toutefois, pour connecter le filtre de convertisseur de mixage vidéo au lieu du convertisseur vidéo, vous devez le spécifier explicitement.

Si vous spécifiez un filtre dans le troisième paramètre, plutôt qu’un code confidentiel, vous devrez peut-être indiquer quelle broche de sortie doit être utilisée pour la connexion. C’est l’objectif des deux premiers paramètres de la méthode. Le premier paramètre s’applique uniquement aux filtres de capture. Il spécifie un GUID qui indique une catégorie de code confidentiel. Pour obtenir la liste complète des catégories, consultez [jeu de propriétés pin](pin-property-set.md). Deux des catégories sont valides pour tous les filtres de capture :

-   **ÉPINGLer la \_ capture de catégorie \_**
-   **Aperçu de la \_ catégorie pin \_**

Si un filtre de capture ne fournit pas de codes confidentiels distincts pour la capture et l’aperçu, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère un filtre [tee intelligent](smart-tee-filter.md) , qui fractionne le flux en un flux de capture et un flux d’aperçu. Du point de vue de l’application, vous pouvez simplement traiter tous les filtres de capture comme ayant des codes confidentiels séparés et ignorer la topologie sous-jacente du graphique.

Pour la capture de fichiers, connectez le code confidentiel de capture à un filtre Mux. Pour l’aperçu instantané, connectez le code confidentiel de l’aperçu à un convertisseur. Si vous permutez les deux catégories, le graphique peut supprimer un nombre excessif de frames pendant la capture de fichier ; Toutefois, si le graphique est correctement connecté, il dépose les images d’aperçu nécessaires pour maintenir le débit sur le flux de capture.

L’exemple suivant montre comment connecter les deux flux :


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Certains filtres de capture prennent également en charge les sous-titres, indiqués par la **catégorie de pin \_ \_ VBI**. Pour capturer les sous-titres dans un fichier, Affichez cette catégorie dans le filtre Mux. Pour afficher les sous-titres dans la fenêtre d’aperçu, connectez-vous au convertisseur :


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



Le deuxième paramètre de [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifie le type de média, et est généralement l’un des éléments suivants :

-   Audio de MEDIATYPE \_
-   Vidéo de MEDIATYPE \_
-   MEDIATYPE \_ entrelacé (DV)

Vous pouvez utiliser ce paramètre chaque fois que les broches de sortie du filtre prennent en charge l’énumération des types de médias préférés. Pour les sources de fichiers, le générateur de graphiques de capture ajoute automatiquement un filtre d’analyseur si nécessaire, puis interroge les types de média sur l’analyseur. (Pour obtenir un exemple, consultez [recompression d’un fichier AVI](recompressing-an-avi-file.md).) En outre, si le dernier filtre de la chaîne a plusieurs broches d’entrée, la méthode tente d’énumérer leurs types de média. Toutefois, tous les filtres ne prennent pas en charge cette fonctionnalité.

## <a name="finding-interfaces-on-filters-and-pins"></a>Recherche d’interfaces sur les filtres et les codes confidentiels

Une fois que vous avez créé un graphique, vous devez généralement Rechercher les différentes interfaces exposées par les filtres et les codes confidentiels dans le graphique. Par exemple, un filtre de capture peut exposer l’interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , tandis que les broches de sortie du filtre peuvent exposer l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .

La façon la plus simple de trouver une interface consiste à utiliser la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) . Cette méthode parcourt le graphique (filtres et codes confidentiels) jusqu’à ce qu’il trouve l’interface souhaitée. Vous pouvez spécifier le point de départ de la recherche, et vous pouvez limiter la recherche aux filtres en amont ou en aval à partir du point de départ.

L’exemple suivant recherche l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sur un code pin d’aperçu vidéo :


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> La rubrique [Rechercher une interface sur un filtre ou un code PIN](find-an-interface-on-a-filter-or-pin.md) affiche une autre approche qui utilise l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) au lieu de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2). L’approche à utiliser dépend de votre application. Si votre application utilise déjà **ICaptureGraphBuilder2** pour générer le graphique, [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) est une bonne approche. Sinon, envisagez d’utiliser les méthodes **IGraphBuilder** .

 

## <a name="finding-pins"></a>Rechercher des broches

Moins souvent, vous devrez peut-être localiser un code confidentiel individuel sur un filtre, bien que dans la plupart des cas, les méthodes [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) et [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) vous éviteront les difficultés. Si vous avez besoin de rechercher un code PIN particulier sur un filtre, la méthode d’assistance [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) est utile. Spécifiez la catégorie, le type de média (vidéo ou audio), la direction et si le code confidentiel doit être déconnecté.

Par exemple, le code suivant recherche un pin de prévisualisation vidéo non connecté sur un filtre de capture :


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 
