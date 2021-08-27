---
description: Cet article contient des conseils pour générer des histogrammes lors du décodage de vidéos à l’aide des API vidéo Direct3D 11 ou 12.
ms.assetid: ''
title: Histogrammes de décodage vidéo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 94371fd68c981a98c4ba629822f928e148c230565b5103dfaa2350543bbe9a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061629"
---
# <a name="direct3d-video-decode-histograms"></a>Histogrammes de décodage vidéo Direct3D

Cet article contient des conseils pour générer des histogrammes lors du décodage de vidéos à l’aide des API vidéo Direct3D 11 ou 12.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Vérification des capacités de l’histogramme dans le périphérique vidéo

Avant de tenter de générer des histogrammes, vous devez vérifier si le périphérique vidéo actuel prend en charge la fonctionnalité d’histogramme décodage vidéo.

### <a name="direct3d-12"></a>Direct3D 12

Appelez [ID3D12VideoDevice :: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) pour vérifier les détails de prise en charge des opérations de décodage vidéo Direct3D 12. Transmettez la valeur **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** à partir de l’énumération [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) pour spécifier que vous demandez la prise en charge des histogrammes de décodage vidéo.

### <a name="direct3d-11"></a>Direct3D 11

Appelez [ID3D11VideoDevice2 :: CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) et transmettez la valeur **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** du [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) pour déterminer si les histogrammes sont pris en charge pour l’appareil actuel.

## <a name="enabling-histogram-during-decode"></a>Activation de l’histogramme durant le décodage

La collection de données d’histogramme est activée par l’appelant en fournissant les mémoires tampons dans lesquelles les données de l’histogramme sont stockées.  Une mémoire tampon de sortie de l’histogramme null pour un composant donné indique que la collection d’histogrammes est désactivée.

### <a name="direct3d-12"></a>Direct3D 12

Pour fournir des tampons de sortie afin de recevoir des données d’histogramme à l’aide de Direct3D 12, vous devez créer votre liste de commandes de décodage à l’aide de la méthode [ID3D12VideoDecodeCommandList1 ::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) . Cette méthode prend une structure [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) comme argument. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** a un champ de type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), qui vous permet de spécifier un [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) dans lequel les données de l’histogramme sont générées.

### <a name="direct3d-11"></a>Direct3D 11

L’interface [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fournit la méthode [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , qui vous permet de fournir une ou plusieurs interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) dans lesquelles les données de l’histogramme seront générées. [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) pour spécifier les composants pour lesquels vous souhaitez que les données de l’histogramme soient générées.


## <a name="buffer-format"></a>Format de la mémoire tampon

La sortie de l’histogramme Decoder est écrite dans une mémoire tampon sous la forme d’un compteur entier par composant.  Le format de la mémoire tampon est une valeur 32 bits par emplacement.  Un appareil peut utiliser une profondeur de bit de compteur entier inférieure à 32 bits, mais doit être de 16, 24 ou 32 bits.  Si c’est le cas, la valeur du compteur est stockée dans les bits inférieurs et les bits inutilisés supérieurs sont nuls.  Lorsque le nombre d’un emplacement dépasse la valeur maximale, l’appareil définit la valeur Max à la place. Les appareils indiquent le nombre d’emplacements pris en charge, qui doit être une valeur de puissance de 2.  Le nombre minimal de casiers requis pour les appareils qui prennent en charge cette fonctionnalité est 64. 

Vous devez fournir une mémoire tampon avec un décalage aligné sur 256 octets et une taille correspondant au nombre d’emplacements pris en charge multiplié par la taille de l’emplacement (4 octets) pour chaque composant demandé.  Le placement des emplacements est déterminé par :

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Quand un format définit les bits utiles d’un composant comme étant inférieurs au nombre de bits de stockage (par exemple, P010 utilise les 10 premiers bits de 16 bits de stockage de composant), seuls les bits utiles sont pris en compte (P010 est traité comme une valeur de 10 bits). 

Le périphérique vidéo signale les composants pris en charge.  Si l’appelant ne souhaite pas un histogramme pour un composant donné, il spécifie nullptr.  Si le pilote ne prend pas en charge un histogramme pour un composant donné, le tampon d’histogramme de ce composant doit être nullptr.

Lorsque plusieurs composants sont pris en charge, l’application peut demander n’importe quelle combinaison de composants par décodage de trame.  Par exemple, si le matériel signale la prise en charge des composants Y, U et V, l’application peut demander l’histogramme Y uniquement pour le frame 1, l’histogramme U uniquement pour le frame 2 et l’histogramme V uniquement pour le frame 3.  Ils peuvent également demander une combinaison de deux composants ou des trois composants.

Les applications fournissent un décalage et un pointeur de mémoire tampon distincts pour chaque composant demandé.  Ce pointeur peut pointer vers la même ressource qu’un autre composant ou une ressource distincte.  Le décalage permet de placer plusieurs composants dans la même mémoire tampon, mais la région de sortie spécifiée par le décalage et la taille de l’histogramme ne doit pas chevaucher une autre sortie de composant d’histogramme.  L’histogramme peut également être écrit dans la même mémoire tampon que d’autres contenus non liés, par exemple en cas d’utilisation dans une stratégie de sous-allocation de ressources.


Le runtime D3D vérifie que les appelants activent uniquement l’histogramme pour les composants pris en charge, que l’offset de la mémoire tampon est aligné et que la taille de la mémoire tampon est suffisante pour le nombre d’emplacements signalés.


## <a name="protected-content"></a>Contenu protégé

Les tampons d’histogramme doivent avoir la même protection de surface que la surface de sortie décode. Si la surface de sortie Decode n’est pas une ressource protégée, le tampon d’histogramme ne doit pas être une ressource protégée. Si la surface de sortie Decode est une ressource protégée, l’histogramme doit être une ressource protégée.








## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>API vidéo Direct3D 
[12](direct3d-12-video-apis.md) 
 [Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




