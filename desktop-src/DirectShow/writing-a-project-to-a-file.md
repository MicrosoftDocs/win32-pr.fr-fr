---
description: écriture d’un Project dans un fichier
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: écriture d’un Project dans un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efea1d0949c419ba6f595e7a381b689d8a8ce69836609d328b555ee695743b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051369"
---
# <a name="writing-a-project-to-a-file"></a>écriture d’un Project dans un fichier

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cet article explique comment écrire un projet de [Services de modification DirectShow](directshow-editing-services.md) dans un fichier. Tout d’abord, il décrit comment écrire un fichier avec le moteur de rendu de base. Il décrit ensuite la recompression intelligente avec le moteur de rendu intelligent.

pour obtenir une vue d’ensemble de la façon dont DirectShow Services d’édition génère le rendu des projets, consultez [à propos des moteurs de rendu](about-the-render-engines.md).

**Utilisation du moteur de rendu de base**

Commencez par créer la partie frontale du graphique, comme suit :

1.  Créez le moteur de rendu.
2.  Spécifiez la chronologie.
3.  Définissez la plage de rendu. (facultatif)
4.  Créez le composant frontal du graphique.

L’exemple de code suivant illustre ces étapes.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Ensuite, ajoutez des filtres de multiplexeur et d’écriture de fichier au graphique de filtre. pour ce faire, le plus simple est de [capturer Graph Builder](capture-graph-builder.md), un composant DirectShow pour générer des graphiques de capture. Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Effectuez les étapes suivantes :

1.  Créez une instance du générateur de graphiques de capture.
2.  Obtenez un pointeur vers le graphique et transmettez-le au générateur de graphiques.
3.  Spécifiez le nom et le type de média du fichier de sortie. Cette étape obtient également un pointeur vers le filtre MUX, qui est requis ultérieurement.

L’exemple de code suivant illustre ces étapes.


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



Enfin, connectez les broches de sortie du serveur frontal au filtre Mux.

1.  Récupérez le nombre de groupes.
2.  Pour chaque code confidentiel, obtenez un pointeur vers le code confidentiel.
3.  Si vous le souhaitez, vous pouvez créer une instance d’un filtre de compression pour compresser le flux. Le type de compresseur dépend du type de média du groupe. Vous pouvez utiliser l' [énumérateur de périphérique système](system-device-enumerator.md) pour énumérer les filtres de compression disponibles. Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).
4.  Éventuellement, définissez des paramètres de compression tels que la fréquence d’images clés. Cette étape est décrite en détail plus loin dans cet article.
5.  Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Cette méthode prend les pointeurs vers le code confidentiel, le filtre de compression (le cas échéant) et le multiplexeur.

L’exemple de code suivant montre comment connecter les broches de sortie.


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



Pour définir les paramètres de compression (étape 4, précédemment), utilisez l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Cette interface est exposée sur les broches de sortie des filtres de compression. Énumérez les codes confidentiels du filtre de compression, puis interrogez chaque broche de sortie pour **IAMVideoCompression**. (Pour plus d’informations sur l’énumération des codes confidentiels, consultez [énumération des codes confidentiels](enumerating-pins.md).) Veillez à libérer tous les pointeurs d’interface que vous avez obtenus lors de cette étape.

Après avoir généré le graphique de filtre, appelez la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) sur le gestionnaire de graphique de filtre. Au fur et à mesure que le graphique de filtre s’exécute, il écrit les données dans un fichier. Utilisez la notification d’événement pour attendre la fin de la lecture. (Consultez [réponse aux événements](responding-to-events.md).) Une fois la lecture terminée, vous devez appeler explicitement [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) pour arrêter le graphique de filtre. Dans le cas contraire, le fichier n’est pas écrit correctement.

**Utilisation du moteur de rendu intelligent**

Pour bénéficier des avantages de la recompression intelligente, utilisez le moteur de rendu intelligent à la place du moteur de rendu de base. Les étapes de création du graphique sont presque les mêmes. La principale différence réside dans le fait que la compression est gérée au premier plan du graphique, et non dans la section d’écriture de fichiers.

> [!IMPORTANT]
> n’utilisez pas le moteur de rendu intelligent pour lire ou écrire Windows fichiers multimédias.

 

Chaque groupe vidéo a une propriété qui spécifie le format de compression pour ce groupe. Le format de compression doit correspondre exactement au format non compressé de la hauteur, de la largeur, de la profondeur de bit et de la fréquence d’images du groupe. Le moteur de rendu intelligent utilise le format de compression lorsqu’il construit le graphique. Avant de définir le format de compression, veillez à définir le format non compressé pour ce groupe en appelant [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md).

Pour définir le format de compression d’un groupe, appelez la méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) . Cette méthode prend un pointeur vers une structure [**SCompFmt0**](scompfmt0.md) . La structure **SCompFmt0** a deux membres : **nFormatId**, qui doit être zéro, et **MediaType**, qui est une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Initialisez la structure du **\_ \_ type de média am** avec les informations de format.

> [!Note]  
> Si vous souhaitez que le projet final ait le même format que l’un de vos fichiers sources, vous pouvez obtenir la \_ structure du type de média am \_ directement à partir du fichier source, à l’aide du détecteur de média. Consultez [**IMediaDet :: obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Effectuez un cast de la variable [**SCompFmt0**](scompfmt0.md) en un pointeur de type **long**, comme indiqué dans l’exemple suivant.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



Le moteur de rendu intelligent recherche automatiquement un filtre de compression compatible. Vous pouvez également spécifier un filtre de compression pour un groupe en appelant [**ISmartRenderEngine :: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Pour générer le graphique, utilisez les mêmes étapes que celles décrites pour le moteur de rendu de base dans la section précédente. Les seules différences sont les suivantes :

-   Utilisez le moteur de rendu intelligent, et non le moteur de rendu de base. L’identificateur de classe est CLSID \_ SmartRenderEngine.
-   Définissez les paramètres de compression après avoir créé le serveur frontal mais avant d’afficher les broches de sortie. Appelez la méthode [**ISmartRenderEngine :: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) pour obtenir un pointeur vers le filtre de compression d’un groupe. Interrogez ensuite l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , comme décrit précédemment.
-   Lorsque vous affichez les broches de sortie, il n’est pas nécessaire d’insérer un filtre de compression. Le flux est déjà compressé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un Project](rendering-a-project.md)
</dt> </dl>

 

 



