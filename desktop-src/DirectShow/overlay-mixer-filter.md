---
description: Filtre du mixeur de superposition
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtre du mixeur de superposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845745"
---
# <a name="overlay-mixer-filter"></a>Filtre du mixeur de superposition

Le filtre de mixage de superposition est un convertisseur vidéo conçu spécifiquement pour la lecture de DVD et la diffusion de flux vidéo avec un sous-titrage de ligne-21. Le mélangeur de superposition prend également en charge les extensions de port vidéo (VPEs), ce qui lui permet de fonctionner avec des décodeurs matériels MPEG-2 ou des tuners TV analogiques qui envoient des vidéos directement à la carte graphique, plutôt que via le bus PCI.

> [!Note]  
> Le [convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) est maintenant préféré par rapport au filtre de mixage de superposition, sauf dans les scénarios VPE.

 

Le mélangeur de superposition utilise DirectDraw pour le rendu. Elle nécessite une surface de recouvrement sur la carte graphique. Le flux vidéo principal doit être connecté à la broche 0. Les flux secondaires (graphiques de sous-titres ou sous-images de DVD) sont connectés aux broches 1 et ultérieure. Le mélangeur de superposition BLITS les flux secondaires directement sur le aire principal ; Il n’effectue pas de mélange ou d’alpha.

Le mélangeur de superposition utilise le convertisseur vidéo pour la gestion des fenêtres. Le convertisseur vidéo se connecte à la broche de sortie du mixer de superposition.

Ce filtre est automatiquement ajouté au graphique de filtre lorsque les applications utilisent les interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) et [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) pour créer le graphique. Le gestionnaire de graphes de filtre n’ajoute pas automatiquement le mélangeur de superposition au graphique.

> [!Note]  
> Dans le tableau suivant, les sous-types de médias acceptés sur la broche d’entrée 0 sont dépendants du matériel. Le mélangeur de superposition ne peut pas déterminer si un sous-type particulier est pris en charge jusqu’à ce qu’il crée la surface DirectDraw. Par conséquent, le seul moyen pour un filtre en amont de déterminer si un sous-type est pris en charge consiste à tenter une connexion avec ce sous-type.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td>Type majeur : MEDIATYPE_Video<br/> Sous-types<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (broche 0 uniquement)</li>
<li>Formats YUV DirectDraw (broche 0 uniquement)</li>
<li>Formats d’accélération vidéo DirectDraw (broche 0 uniquement)</li>
<li>Formats RVB DirectDraw (toutes les broches d’entrée)</li>
</ul>
Types de format :<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (broche 0 uniquement), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection, IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong></strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucune page de propriétés.</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Notes

Le mélangeur de superposition utilise la clé de couleur de destination pour mélanger des surfaces vidéo avec des superpositions. Elle BLITS la clé de couleur et la vidéo secondaire à la surface primaire, puis envoie la vidéo principale à la surface de recouvrement. La carte graphique compose ensuite les deux surfaces dans sa mémoire tampon de trame.

Pour vérifier si le pilote Graphics prend en charge la superposition matérielle, appelez **IDirectDraw7 :: GetCaps**. Si le champ **dwMaxVisibleOverlays** de la structure **DDCAPS** est supérieur à zéro, le pilote prend en charge la superposition matérielle.

Les applications peuvent contrôler certains comportements sur le mélangeur de superposition par le biais de l’interface [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . Les développeurs de jeux peuvent utiliser le mélangeur de superposition pour afficher des vidéos en mode exclusif DirectDraw, comme décrit plus loin dans cette section. Le [filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9) offre désormais une meilleure prise en charge de la vidéo dans les jeux. Pour plus d’informations, consultez [utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md).

Les informations suivantes sont fournies à l’avantage des développeurs de filtres et des développeurs de jeux qui souhaitent utiliser le mélangeur de recouvrement en mode exclusif DirectDraw.

**Opérations internes du mélangeur de superposition**

Le mélangeur de superposition expose une broche d’entrée pour chaque flux entrant. En règle générale, il existe trois broches d’entrée : le code confidentiel 0 pour les données vidéo et les broches 1 et 2 pour les données de sous-image de ligne 21 et de DVD. En interne, le mélangeur de superposition crée un objet DirectDraw avec une surface principale comprenant l’intégralité du bureau, plus une surface de recouvrement dont le rectangle est défini par la taille du flux vidéo sur la broche 0. Si le décodeur ne spécifie pas de clé de couleur, le mélangeur de superposition utilise des clés de couleur par défaut : gris foncé pour les cartes graphiques plus récentes et le magenta pour les plus anciennes cartes de couleur 256.

> [!Note]  
> Les résultats ne sont pas définis si le décodeur remet deux flux vidéo secondaires simultanément à la même place sur la surface de recouvrement. (Cela se produit parfois avec les DVD qui contiennent des flux de sous-image et de ligne 21.) La vidéo peut scintiller ou n’afficher qu’un seul flux.

 

Sur Windows Vista ou version ultérieure, le mélangeur de superposition désactive la composition du Gestionnaire de fenêtrage (DWM) si le pilote d’affichage prend en charge la superposition matérielle. Les applications doivent éviter d’utiliser le filtre de mixage de superposition ; Utilisez VMR-9 ou le convertisseur vidéo amélioré (EVR) à la place.

**Connexion amont avec le décodeur vidéo**

En général, les broches d’entrée du mélangeur de superposition se connectent à un décodeur vidéo en amont. Le flux vidéo principal doit se connecter à la broche 0. La ligne 21 ou les flux de sous-image se connectent à la broche 1 ou supérieure. Si le décodeur est un décodeur logiciel qui utilise exclusivement le processeur hôte, la connexion entre le décodeur et la broche 0 est une connexion [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Si le décodeur utilise l’accélération matérielle, la connexion à la broche 0 doit utiliser le inferface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) . Ces deux types de connexions s’excluent mutuellement.

Si le décodeur crée directement sur la surface de recouvrement, il doit utiliser l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) sur le pin 0 et implémenter l’interface [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

Les filtres qui encapsulent un décodeur matériel et se connectent au mélangeur de superposition via un port vidéo doivent implémenter l’interface [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . Le mélangeur de superposition implémente l’interface [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . Ces deux interfaces permettent au décodeur de spécifier les surfaces de recouvrement nécessaires, et elles permettent au mélangeur de superpositions d’informer le décodeur de l’emplacement de ces surfaces dans la mémoire vidéo.

Le mélangeur de superposition garantit également que le rectangle vidéo est correctement mis à l’échelle. La capture vidéo implique certains problèmes relatifs à la mise à l’échelle de l’image d’aperçu et à la capture d’images vidéo entrelacées. Si vous développez un filtre ou un pilote WDM pour un périphérique de capture vidéo matérielle, reportez-vous aux pages de référence [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) et [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) pour plus d’informations sur ces rubriques.

Le mélangeur de superposition n’est pas utilisé dans les scénarios de capture 1394 ou USB. Il est utilisé lors de la capture vidéo sur le bus PCI.

**Connexion en aval avec le convertisseur vidéo**

Le mélangeur de superposition a une broche de sortie qui se connecte au filtre de [convertisseur vidéo](video-renderer-filter.md) . Dans ce cas, le convertisseur vidéo n’affiche pas la vidéo ; Il gère simplement la fenêtre vidéo.

La connexion de code confidentiel utilise l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) plutôt que l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Le convertisseur vidéo passe son handle de fenêtre par le biais du mélangeur de superposition à DirectDraw, qui gère le découpage de rectangle. Les applications peuvent contrôler le convertisseur vidéo par le biais des interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) sur le gestionnaire de graphique de filtre.

**Mode exclusif DirectDraw**

Le mode DirectDraw en mode exclusif de mixer de superposition permet aux jeux d’afficher des vidéos sur une partie de l’écran. Dans ce mode, le mélangeur de superposition affiche la vidéo directement sur une surface DirectDraw créée par l’application de jeu, plutôt que sur une fenêtre fournie par le convertisseur vidéo. Cela permet aux jeux de contrôler la clé de couleur. Le mélangeur de superposition n’affiche qu’une seule broche d’entrée en mode exclusif DirectDraw, ce qui signifie qu’aucune combinaison de la ligne 21 ou de la sous-image de DVD ne peut être effectuée dans ce mode.

Pour utiliser le mélangeur de superposition en mode exclusif DirectDraw, créez une instance du mélangeur de superposition et interrogez-le pour l’interface [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) avant de générer le graphique de filtre. Appelez ensuite [**IDDrawExclModeVideo :: SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) pour spécifier la surface DirectDraw pour le rendu. Une limitation significative de ce mode est que le jeu n’obtient pas l’accès aux bits vidéo réels. Si vous utilisez **IDDrawExclModeVideo**, votre application crée la surface principale et le mélangeur de superposition crée la surface de recouvrement.

Vous pouvez également utiliser le mode exclusif DirectDraw pour effectuer un rendu sans fenêtre (par exemple, dans une page Web), mais cela n’est pas recommandé, car le mélangeur de superposition n’effectue pas de mélange dans ce mode. Cela signifie qu’aucune donnée de ligne 21 ou de sous-image ne peut être affichée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 




