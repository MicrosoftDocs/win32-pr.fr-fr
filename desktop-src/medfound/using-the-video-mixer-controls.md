---
description: Utilisation des contrôles Video Mixer
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Utilisation des contrôles Video Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034291"
---
# <a name="using-the-video-mixer-controls"></a>Utilisation des contrôles Video Mixer

Le mélangeur EVR fournit plusieurs interfaces qu’une application peut utiliser pour contrôler la façon dont le mélangeur traite la vidéo. Ces interfaces peuvent être utilisées dans DirectShow ou Media Foundation.



| Interface                                                      | Description                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interface [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alpha-fusionne une image bitmap statique sur la vidéo.                                                                                                                                                                                          |
| Interface [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Contrôle la façon dont le EVR mixe les sous-flux vidéo.                                                                                                                                                                                                |
| Interface [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Contrôle l’ajustement des couleurs, les filtres d’images et d’autres fonctionnalités de traitement vidéo. Cette interface fournit l’accès aux fonctionnalités implémentées par le pilote Graphics, de sorte que les fonctionnalités exactes dépendent du pilote Graphics de l’utilisateur. |



 

La méthode correcte pour accéder aux pointeurs vers ces interfaces varie selon que vous utilisez la version DirectShow de EVR ou la version de Media Foundation. Pour le Media Foundation EVR, cela dépend également de l’utilisation directe du EVR ou de son utilisation par le biais de la [session multimédia](media-session.md). (En général, une application utilise EVR via la session multimédia, pas directement).

Pour obtenir un pointeur vers l’une de ces interfaces, procédez comme suit :

1.  Obtient un pointeur vers l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) sur EVR.

    -   Si vous utilisez le filtre DirectShow EVR, appelez **QueryInterface** sur le filtre.

    -   Si vous utilisez directement le récepteur multimédia EVR, appelez **QueryInterface** sur le récepteur multimédia.

    -   Si vous utilisez la session multimédia, appelez **QueryInterface** sur la session multimédia.

2.  Si vous utilisez la session de média, attendez que la session multimédia envoie l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec la valeur d’État MF \_ TOPOSTATUS \_ Ready. (Ignorez cette étape si vous n’utilisez pas la session multimédia.)

3.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour accéder à l’interface de mixage. Utilisez le service de mixage vidéo de l’identificateur de service MR \_ \_ \_ .

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alpha fusion d’une image bitmap sur la vidéo

Vous pouvez utiliser l’interface [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) pour fusionner en alpha une image bitmap statique sur la vidéo pendant la lecture. Vous pouvez stocker l’image bitmap dans une surface Direct3D, spécifiée comme pointeur **IDirect3DSurface9** , ou utiliser une bitmap GDI.

Si vous utilisez une surface Direct3D pour l’image bitmap, celle-ci peut contenir des données alpha par pixel, qui seront utilisées lorsque le mixer alpha-fusionne l’image. Vous pouvez également définir une clé de couleur, c’est-à-dire une couleur transparente qui sera transparente partout où elle apparaîtra dans le bitmap. En outre, vous pouvez spécifier une valeur alpha qui sera appliquée à la totalité de l’image. Vous pouvez également définir un rectangle source pour rogner l’image bitmap et un rectangle de destination pour positionner l’image bitmap dans le cadre de la vidéo.

Pour définir la bitmap, appelez [**IMFVideoMixerBitmap :: SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Cette méthode prend un pointeur vers une structure [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) qui spécifie l’image bitmap et les paramètres de fusion alpha. Pour obtenir un exemple de code, consultez la rubrique de référence pour la méthode **SetAlphaBitmap** .

Une fois que vous avez défini la bitmap, vous pouvez mettre à jour les paramètres de fusion, y compris les recangles source et de destination, en appelant [**IMFVideoMixerBitmap :: UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). La mise à jour est appliquée à la prochaine image vidéo. La vidéo doit être lue pour que la mise à jour se produise. Vous pouvez utiliser cette méthode pour exécuter des animations simples sur l’image bitmap. (Si vous avez besoin d’effets plus sophistiqués, envisagez d’écrire un mélangeur EVR personnalisé.)

Pour effacer la bitmap, appelez [**IMFVideoMixerBitmap :: ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Contrôle des sous-flux

Le EVR peut combiner un ou plusieurs sous-flux vidéo sur le flux vidéo principal. Pour contrôler le mixage de sous-flux, utilisez l’interface [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) .

-   Appelez [**IMFVideoMixerControl :: SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) pour définir la position d’un sous-flux dans le cadre vidéo composite.

-   Appelez [**IMFVideoMixerControl :: SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) pour définir l’ordre de plan pour les sous-flux. Le EVR dessine les flux vidéo dans l’ordre de leurs valeurs d’ordre de plan, en commençant par zéro. Le flux vidéo principal est toujours en premier dans l’ordre de plan.

## <a name="video-processor-settings"></a>Paramètres du processeur vidéo

Le mélangeur EVR utilise l’accélération vidéo DirectX (DXVA) pour effectuer le traitement vidéo sur les flux d’entrée. Les fonctionnalités de traitement exactes dépendent du pilote Graphics. Les fonctionnalités de traitement vidéo sont décrites à l’aide de la structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) . Un ensemble de fonctionnalités particulier est appelé *mode de traitement vidéo*, chaque mode étant identifié par un GUID. Pour obtenir la liste des GUID prédéfinis, consultez [**IDirectXVideoProcessorService :: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). Le pilote peut définir des GUID supplémentaires spécifiques au fournisseur, représentant différentes combinaisons de fonctionnalités.

Pour rechercher les modes pris en charge et les fonctionnalités de chaque mode, procédez comme suit :

1.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) du mixer.

2.  Appelez [**IMFVideoProcessor :: GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Cette méthode retourne un tableau de GUID qui identifient les modes de processeur vidéo disponibles. La liste est retournée dans l’ordre de qualité décroissant, le mode avec la qualité la plus élevée apparaissant en premier dans la liste. La liste peut varier en fonction du format de la vidéo.

3.  Pour chaque GUID de la liste, appelez [**IMFVideoProcessor :: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) pour rechercher les fonctionnalités du mode de processeur vidéo correspondant. La méthode remplit une structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) avec une description des fonctionnalités.

4.  Pour sélectionner un mode, appelez [**IMFVideoProcessor :: SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). Dans le cas contraire, le EVR sélectionne automatiquement un mode au démarrage de la diffusion en continu. Dans ce cas, vous pouvez appeler [**IMFVideoProcessor :: GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) pour rechercher le mode sélectionné.

La plupart des champs de la structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) décrivent le comportement de pilote de bas niveau et ne sont pas intéressants dans une application classique. Les champs suivants sont susceptibles d’intéresser :

-   **DeviceCaps**. Ce champ indique si le traitement vidéo est effectué dans le matériel ou les logiciels, et si le pilote Graphics est un ancien pilote DXVA 1,0.

-   **DeinterlaceTechnology**. Ce champ fournit une indication du niveau de qualité de désentrelacement que vous pouvez attendre si la vidéo source est entrelacée.

-   **ProcAmpControlCaps**. Ce champ spécifie les contrôles d’ajustement des couleurs disponibles. Pour obtenir la liste des ajustements de couleurs possibles, consultez [paramètres de ProcAmp](procamp-settings.md). Si le pilote ne peut pas effectuer le réglage des couleurs, ce champ est égal à zéro.

-   **VideoProcessorOperations**. Ce champ contient des indicateurs qui décrivent les diverses fonctionnalités de traitement vidéo. Deux indicateurs revêtant une importance particulière sont l’indicateur de sous-flux de DXVA2 \_ VideoProcess et l’indicateur de sous-flux de données \_ \_ VideoProcess DXVA2 \_ . Au moins un de ces indicateurs doit être présent pour que le EVR mélange les sous-flux dans le flux vidéo de référence. Si aucun indicateur n’est présent, le EVR est limité à un flux vidéo.

-   **NoiseFilterTechnology**. Ce champ indique les filtres de bruit pris en charge par le pilote Graphics. Si le pilote ne prend pas en charge le filtrage de bruit, la valeur est DXVA2 \_ NoiseFilterTech non \_ pris en charge.

-   **DetailFilterTechnology**. Ce champ indique quels filtres de détails sont pris en charge par le pilote Graphics. Si le pilote ne prend pas en charge le filtrage de bruit, la valeur est DXVA2 \_ DetailFilterTech non \_ pris en charge.

## <a name="color-adjustment-and-image-filtering"></a>Réglage des couleurs et filtrage des images

Le pilote Graphics peut prendre en charge le réglage des couleurs (également appelé *amplification de processus* ou simplement *ProcAmp*) et le filtrage d’images. Lorsqu’il est effectué par le GPU, le réglage des couleurs et le filtrage des images peuvent être effectués en temps réel sans surcharge du processeur.

Pour utiliser ces fonctionnalités, procédez comme suit :

1.  Sélectionnez un mode de traitement vidéo comme décrit dans la section précédente.

2.  Appelez [**IMFVideoProcessor :: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) pour rechercher les fonctionnalités de traitement vidéo, comme décrit dans la section précédente. La méthode remplit une structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) qui décrit les fonctionnalités, notamment si le pilote prend en charge le réglage des couleurs et le filtre d’images.

3.  Pour chaque réglage des couleurs pris en charge par le pilote, appelez [**IMFVideoProcessor :: GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) pour rechercher la plage de valeurs possibles pour ce paramètre. Cette méthode retourne également la valeur par défaut pour le paramètre. Appelez [**IMFVideoProcessor :: GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) pour rechercher la valeur actuelle des paramètres. Les valeurs n’ont pas d’unités spécifiées. Il revient au pilote de définir la plage de valeurs.

4.  Appelez [**IMFVideoProcessor :: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) pour définir une valeur de réglage des couleurs.

5.  Si le pilote prend en charge le filtrage d’images, chaque type de filtre (bruit et détail) prend en charge trois paramètres (niveau, rayon et seuil) à la fois dans la couleur et la luminance. (Consultez [paramètres de filtre d’image DXVA](dxva-image-filter-settings.md).) Pour chaque paramètre, appelez [**IMFVideoProcessor :: GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) pour obtenir la plage de valeurs possibles et appelez [**IMFVideoProcessor :: GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) pour obtenir la valeur actuelle.

6.  Pour modifier un paramètre de filtre d’image, appelez [**IMFVideoProcessor :: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 



