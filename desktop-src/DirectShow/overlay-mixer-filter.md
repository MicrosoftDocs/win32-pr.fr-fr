---
description: Filtre du mixeur de superposition
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtre du mixeur de superposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b4134221efd43bdc2d72e864508440f7a105db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312353"
---
# <a name="overlay-mixer-filter"></a>Filtre du mixeur de superposition

le filtre de Mixer de superposition est un convertisseur vidéo conçu spécifiquement pour la lecture de DVD et la diffusion de flux vidéo avec un sous-titrage de ligne-21. le Mixer de superposition prend également en charge les Extensions de Port vidéo (VPEs), ce qui lui permet de fonctionner avec des décodeurs matériels MPEG-2 ou des tuners TV analogiques qui envoient des vidéos directement à la carte graphique, plutôt que via le bus PCI.

> [!Note]  
> le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) est maintenant préféré à la superposition Mixer filtre, sauf dans les scénarios VPE.

 

le Mixer de superposition utilise DirectDraw pour le rendu. Elle nécessite une surface de recouvrement sur la carte graphique. Le flux vidéo principal doit être connecté à la broche 0. Les flux secondaires (graphiques de sous-titres ou sous-images de DVD) sont connectés aux broches 1 et ultérieure. la superposition Mixer blits les flux secondaires directement sur le aire principal ; Il n’effectue pas de mélange ou d’alpha.

le Mixer de superposition utilise le convertisseur vidéo pour la gestion des fenêtres. le convertisseur vidéo se connecte à la broche de sortie de l’Mixer de recouvrement.

Ce filtre est automatiquement ajouté au graphique de filtre lorsque les applications utilisent les interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) et [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) pour créer le graphique. le gestionnaire de Graph de filtre n’ajoute pas automatiquement les Mixer de superposition au graphique.

> [!Note]  
> Dans le tableau suivant, les sous-types de médias acceptés sur la broche d’entrée 0 sont dépendants du matériel. le Mixer de superposition ne peut pas déterminer si un sous-type particulier est pris en charge jusqu’à ce qu’il crée la surface DirectDraw. Par conséquent, le seul moyen pour un filtre en amont de déterminer si un sous-type est pris en charge consiste à tenter une connexion avec ce sous-type.

 




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | 
| Types de média de broche d’entrée | Type majeur : MEDIATYPE_Video<br /> Sous-types<br /><ul><li>MEDIASUBTYPE_Overlay (broche 0 uniquement)</li><li>Formats YUV DirectDraw (broche 0 uniquement)</li><li>Formats d’accélération vidéo DirectDraw (broche 0 uniquement)</li><li>Formats RVB DirectDraw (toutes les broches d’entrée)</li></ul>Types de format :<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | 
| Interfaces pin d’entrée | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (broche 0 uniquement), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection, IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong></strong></a> | 
| Types de média de broche de sortie | MEDIATYPE_Video, MEDIASUBTYPE_Overlay | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_OverlayMixer | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | qdvd.dll | 
| <a href="merit.md">Mérite</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Remarques

le Mixer de superposition utilise la clé de couleur de destination pour mélanger des surfaces vidéo avec des superpositions. Elle BLITS la clé de couleur et la vidéo secondaire à la surface primaire, puis envoie la vidéo principale à la surface de recouvrement. La carte graphique compose ensuite les deux surfaces dans sa mémoire tampon de trame.

Pour vérifier si le pilote Graphics prend en charge la superposition matérielle, appelez **IDirectDraw7 :: GetCaps**. Si le champ **dwMaxVisibleOverlays** de la structure **DDCAPS** est supérieur à zéro, le pilote prend en charge la superposition matérielle.

les Applications peuvent contrôler certains comportements sur la superposition Mixer par le biais de l’interface [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . les développeurs de jeux peuvent utiliser la superposition Mixer pour afficher les vidéos en Mode exclusif DirectDraw, comme décrit plus loin dans cette section. Le [filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9) offre désormais une meilleure prise en charge de la vidéo dans les jeux. Pour plus d’informations, consultez [utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md).

les informations suivantes sont fournies à l’avantage des développeurs de filtres et des développeurs de jeux qui souhaitent utiliser la superposition Mixer en Mode exclusif DirectDraw.

**superposition Mixer opérations internes**

le Mixer de superposition expose une broche d’entrée pour chaque flux entrant. En règle générale, il existe trois broches d’entrée : le code confidentiel 0 pour les données vidéo et les broches 1 et 2 pour les données de sous-image de ligne 21 et de DVD. en interne, le Mixer de superposition crée un objet DirectDraw avec une surface principale comprenant l’intégralité du bureau, plus une surface de recouvrement dont le rectangle est défini par la taille du flux vidéo sur la broche 0. si le décodeur ne spécifie pas de clé de couleur, le Mixer de recouvrement utilise des clés de couleur par défaut : gris foncé pour les cartes graphiques plus récentes et le magenta pour les plus anciennes cartes de couleur 256.

> [!Note]  
> Les résultats ne sont pas définis si le décodeur remet deux flux vidéo secondaires simultanément à la même place sur la surface de recouvrement. (Cela se produit parfois avec les DVD qui contiennent des flux de sous-image et de ligne 21.) La vidéo peut scintiller ou n’afficher qu’un seul flux.

 

sur Windows Vista ou version ultérieure, la superposition Mixer désactive la composition du Gestionnaire de fenêtrage (DWM) si le pilote d’affichage prend en charge la superposition matérielle. les Applications doivent éviter d’utiliser le filtre de Mixer de recouvrement ; Utilisez VMR-9 ou le convertisseur vidéo amélioré (EVR) à la place.

**Connexion amont avec le décodeur vidéo**

en général, les broches d’entrée du Mixer de superposition se connectent à un décodeur vidéo en amont. Le flux vidéo principal doit se connecter à la broche 0. La ligne 21 ou les flux de sous-image se connectent à la broche 1 ou supérieure. Si le décodeur est un décodeur logiciel qui utilise exclusivement le processeur hôte, la connexion entre le décodeur et la broche 0 est une connexion [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Si le décodeur utilise l’accélération matérielle, la connexion à la broche 0 doit utiliser le inferface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) . Ces deux types de connexions s’excluent mutuellement.

Si le décodeur crée directement sur la surface de recouvrement, il doit utiliser l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) sur le pin 0 et implémenter l’interface [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

les filtres qui encapsulent un décodeur matériel et se connectent à la superposition Mixer via un port vidéo doivent implémenter l’interface [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . le Mixer de superposition implémente l’interface [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . ces deux interfaces permettent au décodeur de spécifier les surfaces de superposition qu’il requiert, et elles permettent au décodeur de Mixer d’informer le décodeur de l’emplacement de ces surfaces dans la mémoire vidéo.

le Mixer de superposition garantit également que le rectangle vidéo est correctement mis à l’échelle. La capture vidéo implique certains problèmes relatifs à la mise à l’échelle de l’image d’aperçu et à la capture d’images vidéo entrelacées. Si vous développez un filtre ou un pilote WDM pour un périphérique de capture vidéo matérielle, reportez-vous aux pages de référence [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) et [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) pour plus d’informations sur ces rubriques.

le Mixer de superposition n’est pas utilisé dans les scénarios de capture 1394 ou USB. Il est utilisé lors de la capture vidéo sur le bus PCI.

**Connexion en aval avec le convertisseur vidéo**

le Mixer de recouvrement a une broche de sortie qui se connecte au filtre de [convertisseur vidéo](video-renderer-filter.md) . Dans ce cas, le convertisseur vidéo n’affiche pas la vidéo ; Il gère simplement la fenêtre vidéo.

La connexion de code confidentiel utilise l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) plutôt que l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . le convertisseur vidéo passe son handle de fenêtre par le biais de la superposition Mixer à DirectDraw, qui gère le découpage de rectangle. les Applications peuvent contrôler le convertisseur vidéo par le biais des interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) sur le gestionnaire de Graph de filtre.

**Mode exclusif DirectDraw**

le mode en mode exclusif DirectDraw de Mixer de superposition permet aux jeux d’afficher des vidéos sur une partie de l’écran. dans ce mode, le Mixer de superposition affiche la vidéo directement sur une surface DirectDraw créée par l’application de jeu, plutôt que sur une fenêtre fournie par le convertisseur vidéo. Cela permet aux jeux de contrôler la clé de couleur. le Mixer de superposition expose une seule broche d’entrée en mode exclusif DirectDraw, ce qui signifie qu’aucune combinaison de la ligne 21 ou de la sous-image de DVD ne peut être effectuée dans ce mode.

pour utiliser la superposition Mixer en mode exclusif DirectDraw, créez une instance de la superposition Mixer et interrogez-la pour l’interface [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) avant de générer le graphique de filtre. Appelez ensuite [**IDDrawExclModeVideo :: SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) pour spécifier la surface DirectDraw pour le rendu. Une limitation significative de ce mode est que le jeu n’obtient pas l’accès aux bits vidéo réels. si vous utilisez **IDDrawExclModeVideo**, votre application crée la surface principale, et la superposition Mixer crée la surface de recouvrement.

vous pouvez également utiliser le mode exclusif DirectDraw pour effectuer un rendu sans fenêtre (par exemple, dans une page Web), mais cela n’est pas recommandé, car le chevauchement Mixer n’effectue pas de mélange dans ce mode. Cela signifie qu’aucune donnée de ligne 21 ou de sous-image ne peut être affichée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




