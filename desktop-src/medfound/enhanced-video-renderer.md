---
description: Le convertisseur vidéo amélioré (EVR) est un composant qui affiche la vidéo sur le moniteur des utilisateurs.
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: Convertisseur vidéo amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317973"
---
# <a name="enhanced-video-renderer"></a>Convertisseur vidéo amélioré

Le convertisseur vidéo amélioré (EVR) est un composant qui affiche la vidéo sur l’écran de l’utilisateur. Il existe deux versions du EVR :

-   Récepteur multimédia EVR pour les applications Media Foundation.
-   Le filtre EVR pour les applications DirectShow.

Les deux versions utilisent les mêmes objets internes pour effectuer le rendu de la vidéo, et elles partagent un grand nombre des mêmes interfaces.

Le EVR peut combiner jusqu’à 16 flux vidéo. Le premier flux d’entrée est appelé le *flux de référence*. Le flux de référence apparaît toujours en premier dans l’ordre de plan. Tous les flux supplémentaires sont appelés des sous- *flux* et sont mélangés au-dessus du flux de référence. L’application peut modifier l’ordre de plan des sous-flux, mais aucun sous-flux ne peut être d’abord dans l’ordre de plan.

Le pilote Graphics détermine les formats vidéo pris en charge, mais ils sont généralement limités aux éléments suivants :

-   Flux de référence : YUV progressif ou entrelacé, sans alpha par pixel (comme NV12 ou YUY2); ou RGB progressif.
-   Sous-flux : YUV progressifs avec par pixel-alpha, tels que AYUV ou AI44.

Les formats de sous-flux disponibles peuvent dépendre du format du flux de référence. Pour plus d’informations, consultez [EVR Media type Negotiation](evr-media-type-negotiation.md).

En interne, EVR utilise un objet appelé *mixer* pour combiner les frames des flux d’entrée sur une surface de rendu. Le mélangeur effectue également une correction de désentrelacement et de couleur. La sortie du mélangeur est la dernière image vidéo composite. Un deuxième objet appelé le *présentateur* restitue le cadre vidéo à l’affichage. Le présentateur planifie le rendu des frames et gère l’appareil Direct3D. Une application peut fournir une implémentation personnalisée du mélangeur ou du présentateur.

La fréquence d’images de sortie est verrouillée dans le flux de référence. Chaque fois que les sous-flux reçoivent de nouvelles images, le mélangeur les conserve. Lorsque le flux de référence reçoit un nouveau Frame, le mixer composite ce frame avec les frames de sous-flux. (Si le flux de référence est entrelacé, une trame de référence complète peut nécessiter plusieurs exemples de supports.) Il est possible qu’un sous-flux reçoive plusieurs frames alors que le mixer attend un frame de référence. Dans ce cas, le mélangeur ignore simplement le frame de sous-flux précédent.

Étant donné que le présentateur crée le périphérique Direct3D, il est également chargé de partager l’appareil avec d’autres objets de pipeline qui doivent accéder aux services d’accélération vidéo DirectX (DXVA). En particulier, le mélangeur EVR utilise les services de traitement vidéo DXVA pour désentrelacer et mélanger la vidéo. Externe au EVR, les décodeurs logiciels peuvent utiliser DXVA pour le décodage vidéo accéléré. Le présentateur partage le périphérique Direct3D au moyen du [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md). Le diagramme suivant illustre l’architecture interne de EVR. (Le décodeur logiciel, ombré en gris, ne fait pas partie du EVR.)

![diagramme architectural montrant le EVR.](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>Interfaces EVR

Le EVR prend en charge les interfaces suivantes. Certaines de ces interfaces sont implémentées par le mélangeur ou le présentateur. Pour chaque interface, la rubrique de référence explique comment obtenir un pointeur vers l’interface.

| Interface                                                    | Description                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | Définit le nombre de broches d’entrée sur le filtre EVR (DirectShow uniquement).                                |
| [**IEVRFilterConfigEx**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | Configure le filtre EVR (DirectShow uniquement).                                                      |
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | Permet à un plug-in EVR de restituer une vidéo protégée.                                                 |
| [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | Permet au présentateur EVR de demander un frame spécifique à partir du mélangeur.                             |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | Permet au gestionnaire de qualité d’ajuster la qualité vidéo EVR.                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | Permet à un mélangeur ou un présentateur personnalisé d’obtenir des pointeurs d’interface à partir du EVR.                       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | Retourne l’identificateur d’appareil d’un mélangeur ou d’un présentateur EVR.                                       |
| [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | Contrôle la façon dont le EVR affiche la vidéo.                                                              |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alpha-fusionne une image bitmap statique avec la vidéo.                                                |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | Contrôle la façon dont le convertisseur de vidéo amélioré (EVR) mixe les sous-flux vidéo.                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | Contrôle les préférences pour le désentrelacement vidéo.                                                     |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | Mappe une position sur un flux vidéo d’entrée à la position correspondante sur un flux vidéo de sortie. |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | Exposé par le présentateur EVR.                                                                     |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | Contrôle le traitement vidéo, y compris les réglages, les filtres de bruit et les filtres de détails.               |
| [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | Définit un mélangeur ou un présentateur sur le EVR.                                                             |
| [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | Alloue des exemples vidéo.                                                                          |



 

## <a name="in-this-section"></a>Dans cette section



| Rubrique                                                                    | Description                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Utilisation du filtre DirectShow EVR](using-the-directshow-evr-filter.md)   | Comment utiliser EVR dans une application DirectShow.                                       |
| [Utilisation du récepteur multimédia EVR](using-the-evr-media-sink.md)                 | Comment utiliser EVR dans une application Media Foundation.                                 |
| [Utilisation des contrôles d’affichage vidéo](using-the-video-display-controls.md) | Comment contrôler la façon dont le EVR affiche la vidéo dans la fenêtre d’application. |
| [Utilisation des contrôles Video Mixer](using-the-video-mixer-controls.md)     | Comment contrôler la façon dont le mélangeur EVR fonctionne.                               |
| [Négociation de type de média EVR](evr-media-type-negotiation.md)             | Décrit comment le EVR détermine les formats vidéo qu’il peut accepter comme entrée.          |
| [Mélangeurs personnalisés](custom-mixers.md)                                       | Comment écrire un mélangeur personnalisé pour EVR.                                              |
| [Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md)       | Comment écrire un présentateur personnalisé pour EVR.                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 



