---
description: Utilisation de la catégorie d’images Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Utilisation de la catégorie d’images Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531458"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Utilisation de la catégorie d’images Windows Media Video 9,1

La catégorie d’images Windows Media Video 9,1 est différente des autres catégories de sortie prises en charge par l’encodeur et le décodeur Windows Media Video 9. Au lieu de traiter une vidéo non compressée, elle prend des échantillons d’entrée spéciaux qui se composent de données de transformation structurées et, parfois, d’images bitmap RVB sur lesquelles les transformations sont effectuées.

Le contenu d’image Windows Media Video 9,1 encodé est quasiment identique au contenu encodé normal Windows Media Video 9, mais il est identifié par son propre code FOURCC (« WMVP »).

Le type de sortie de l’encodeur pour l’image vidéo est défini exactement de la même façon que la vidéo Windows Media standard, sauf que les valeurs de sous-type et de compression doivent être définies sur les identificateurs d’image vidéo. Cela comprend la nécessité d’obtenir des données privées de codec et de les ajouter à la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Pour plus d’informations, consultez Configuration de l' [encodage vidéo](configuringvideoencoding.md).

La configuration du type d’entrée pour l’image vidéo est également très similaire à la configuration d’entrée pour les autres encodeurs vidéo. Vous pouvez récupérer un [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) partiellement terminé à partir de l’encodeur en appelant [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), ou si vous utilisez le kit de développement logiciel (SDK) Media Foundation, en appelant [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) et en extrayant le **\_ \_ type de média DMO** à l’aide de [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Vous définissez ensuite la taille du frame et la structure du format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , comme vous le feriez pour une vidéo standard. Comme pour le type de sortie, vous devez vous assurer que les valeurs de sous-type et de compression sont correctement définies.

## <a name="creating-input-samples"></a>Création d’exemples d’entrée

Les exemples d’entrée du codec d’image vidéo sont structurés. La définition de la structure et des constantes utilisées pour l’image vidéo n’est pas fournie avec les interfaces de codec vidéo et Windows Media Audio. Ces définitions sont incluses dans le kit de développement logiciel (SDK) Windows Media format et leur utilisation est entièrement expliquée dans la documentation du kit de développement logiciel (SDK) Windows Media format.

## <a name="decoding"></a>Décodage

Il n’existe aucune exigence particulière pour décoder la vidéo de capture d’écran. À part un sous-type différent (MEDIASUBTYPE \_ WMVP) utilisé pour l’entrée du décodeur, le flux de l’image vidéo compressée est fondamentalement identique à un flux de Windows Media Video standard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 
