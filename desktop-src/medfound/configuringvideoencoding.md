---
description: Configuration de l’encodage vidéo
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configuration de l’encodage vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111834"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configuration de l’encodage vidéo (Microsoft Media Foundation)

Pour configurer l’encodeur vidéo, procédez comme suit :

1.  Définissez des propriétés sur l’encodeur DMO à l’aide de **IPropertyBag :: Write**. La liste suivante résume l’ensemble minimal des propriétés requises pour encoder un flux vidéo CBR (toutes ces valeurs ont des valeurs par défaut qui peuvent être utilisées) :

    -   La propriété[MFPKEY \_ VIDEOWINDOW](mfpkey-videowindowproperty.md) spécifie la fenêtre de mémoire tampon à utiliser pour le flux. Pour plus d’informations sur le paramètre Windows de mémoire tampon et son impact sur le contenu, consultez [méthodes d’encodage](encodingmethods.md). La fenêtre de mémoire tampon par défaut est de trois secondes, ce qui convient à de nombreux scénarios.
    -   La complexité vidéo est définie pour déterminer le compromis entre la qualité du contenu encodé et le temps nécessaire à l’encodage. Si vous ne définissez pas de valeur, la valeur par défaut est utilisée. Toutefois, vous pouvez trouver les modes recommandés pour un codec spécifique en appelant [IWMCodecProps :: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) pour récupérer g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline et g \_ wszWMVCComplexityExMax. Vous pouvez ensuite définir [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) sur une valeur comprise entre 0 et la complexité maximale signalée.
    -   [MFPKEY \_ CRISP](mfpkey-crispproperty.md) spécifie l’importance relative du lissage vidéo et la qualité d’image des frames encodés. Dans la plupart des cas, la valeur par défaut fonctionne correctement.
    -   Pour le contenu vidéo stocké dans un conteneur autre que ASF, la propriété [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md) doit avoir la valeur 0. Il ne s’agit pas de la valeur par défaut.

    Pour plus d’informations sur la configuration des flux VBR, consultez [utilisation de l’encodage VBR](usingvbrencoding.md).

2.  Configurez la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) pour le type d’entrée, ou si vous utilisez le kit de développement logiciel (SDK) Media Foundation, utilisez la fonction [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Utilisez une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) décrivant le contenu d’entrée non compressé. Le codec ne redimensionne pas la vidéo ou ne convertit pas l’espace colorimétrique.
3.  Définissez le type d’entrée à l’aide de [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) ou [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configurez le type de sortie pour l’encodeur. Une fois que le type d’entrée est défini, l’encodeur énumère les types de sortie qui sont complets, à l’exception du membre **dwBitrate** de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , ou de l’attribut de [**vitesse de \_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) de l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Si vous récupérez un type de sortie avant de définir un type d’entrée, la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) fournie n’a pas de **VIDEOINFOHEADER** associé.
5.  Récupérez les données privées du codec et ajoutez-les à la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que vous transmettez à la structure du [](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) ou à IMFMediaType. Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).
6.  Définissez le type de sortie en appelant la méthode [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) ou [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Transmettez la structure du [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) avec la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) terminée (y compris les données privées ajoutées) référencées dans le membre **pbFormat** , ou construisez un [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) en appelant [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> L’objet encodeur vidéo prend en charge deux sorties. La deuxième sortie est pour l’encodeur « affichage de la publication ». Il fournit les exemples non compressés tels qu’ils seront fournis par le décodeur. Cela vous permet de surveiller la qualité de l’encodage sans avoir à attendre que le flux entier soit traité. Cette sortie est facultative. Si vous souhaitez l’utiliser, configurez son type suivant le même processus que celui utilisé pour définir le type d’entrée de l’encodeur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 
