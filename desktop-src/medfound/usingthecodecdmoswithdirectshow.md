---
description: Utilisation des codecs multimédias Windows dans DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Utilisation des codecs multimédias Windows dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518136"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Utilisation des codecs multimédias Windows dans DirectShow

Les objets d’encodeur et de décodeur Windows Media Audio et vidéo ont été initialement conçus et optimisés pour fonctionner avec le format de conteneur de fichiers ASF et le kit de développement logiciel (SDK) du format Windows Media. Les objets codec fonctionnent correctement dans DirectShow pour certains scénarios, à savoir un encodage CBR et un encodage VBR basé sur la qualité des flux vidéo. Toutefois, si vous envisagez d’utiliser les objets codec directement dans DirectShow en utilisant des conteneurs de fichiers autres que ASF, vous devez connaître à l’avance certains comportements et problèmes.

> [!Note]  
> Si vous envisagez d’utiliser des codecs autonomes avec DirectShow, vous souhaiterez probablement les utiliser en tant que DMOs uniquement. En d’autres termes, vous allez utiliser l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) au lieu de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Fichier audio WM dans les fichiers AVI

Vous pouvez utiliser DirectShow pour encoder des flux WMA dans n’importe quel format de conteneur de fichiers pour lequel vous disposez d’un filtre multiplexeur. Toutefois, les interfaces de codec vidéo et Windows Media Audio ne prennent pas en charge WMA dans les fichiers AVI, car il est impossible d’utiliser les filtres de lecture AVI par défaut pour maintenir la synchronisation audio-vidéo dans un fichier AVI avec un flux WMA. Pour plus d’informations, consultez [stockage de médias compressés dans des fichiers AVI](storingcompressedmediainavifiles.md).

L’encodeur audio DMO génère des échantillons de durée variable, même en mode « taux binaire constant ». Cela fonctionne donc mieux avec les formats de conteneur de fichiers qui utilisent des horodatages. Les fichiers AVI ne fournissent pas d’horodatage pour chaque exemple audio ou groupe d’exemples. Dans DirectShow, le filtre de séparateur AVI fabrique des horodatages pour chaque groupe d’échantillons (chaque bloc audio) en fonction de la valeur **nAvgBytesPerSec** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dans l’en-tête de flux avi.

L’hypothèse sous-jacente à ce calcul est que tous les échantillons audio dans le flux sont de même durée ; Toutefois, les exemples générés par DMO ne sont pas de la même durée, et les horodatages appliqués par le séparateur AVI ne sont pas exacts. Par conséquent, il n’est pas possible, sans modifier le séparateur AVI ou le décodeur audio DMO, d’utiliser une application DirectShow pour lire les fichiers AVI avec des flux audio et vidéo synchronisés. Le codec vocal Windows Media Audio 9 fonctionne dans certains cas, mais même si cela perd la synchronisation après toute opération de recherche, il ne peut pas être considéré comme une solution viable.

Si vous disposez d’un encodeur MP3, vous pouvez créer des fichiers AVI avec WMV et MP3 pour le flux audio. Ces fichiers sont lus et se recherchent correctement dans le lecteur Windows Media et d’autres applications DirectShow, car le séparateur AVI contient du code de gestion spécial pour les flux MP3. Une autre option consiste à utiliser l’audio PCM non compressé, bien que la taille du fichier résultant soit nettement supérieure à celle d’un flux audio compressé. Étant donné que l’exemple d’application DirectShow crée des fichiers AVI, il ne montre pas comment utiliser l’encodeur audio DMO.

## <a name="one-pass-encoding"></a>Encodage à passage unique

L’encodeur vidéo DMO fonctionne facilement dans DirectShow pour deux modes d’encodage : CBR et VBR basé sur la qualité. Tant que vous suivez l’ordre correct des opérations lors de la génération du graphique de filtre, comme illustré dans l’exemple d’application, il est relativement simple de placer du contenu WMV dans un fichier AVI à l’aide du multiplexeur AVI et du writer de fichier.

## <a name="two-pass-encoding"></a>Encodage en deux passes

Les modes d’encodage à deux passes nécessitent une approche plus complexe de la génération et de la diffusion de graphiques afin d’empêcher la réinitialisation de son contenu à partir de la première passe avant de commencer la deuxième. Dans l’encodage en deux passes, il est nécessaire d’exécuter le graphique une seule fois pour que la solution DMO puisse effectuer son analyse de prétraitement des données de fichier, puis Rembobiner le graphique et l’exécuter à nouveau afin que la solution DMO puisse effectuer l’encodage réel.

Lorsque le graphique passe à l’état d’exécution pour la deuxième passe, le wrapper DMO définit l’indicateur de discontinuité sur le premier exemple, car l’horodatage n’est pas séquentiel avec le dernier horodatage sur la première passe. Lorsque la solution DMO, qui n’a pas été conçue pour fonctionner dans DirectShow, reçoit l’indicateur de discontinuité, elle effectue un vidage et perd les données stockées à partir de la première passe. Pour contourner ce problème, la meilleure solution consiste probablement à écrire un filtre de wrappers DMO personnalisé qui ne définit pas l’indicateur de discontinuité lorsque le graphique est cherché après la première passe. L’exemple Video for Windows (VfW) dans ce kit de développement logiciel (SDK) montre comment effectuer un encodage en deux passes.

## <a name="interlaced-content"></a>Contenu entrelacé

L’encodeur WMV est capable d’encoder du contenu entrelacé tout en préservant l’entrelacement, ce qui est utile pour le contenu capturé à partir d’un téléviseur et peut également être lu sur un téléviseur. Toutefois, il n’est pas possible de conserver l’entrelacement à l’aide du wrapper DMO par défaut, car ce filtre ne prend pas en charge [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) sur ses exemples d’entrée.

La DMO utilise cette interface pour obtenir les paramètres entrelacés pour chaque exemple qu’elle reçoit. Si l’interface est introuvable, comme c’est le cas avec le wrapper DMO, DMO traite simplement les exemples d’entrée comme non entrelacés. Pour effectuer un encodage entrelacé dans DirectShow, il existe plusieurs alternatives. L’approche la plus simple consiste probablement à utiliser le kit de développement logiciel (SDK) de la série Windows Media Format 9 directement ou à l’aide du filtre DirectShow de l’enregistreur ASF pour créer un fichier ASF entrelacé. Vous pouvez ensuite transcoder ce fichier dans un autre format. Si vous transcodez dans AVI, vous disposerez d’un fichier entrelacé, mais les filtres de lecture AVI standard DirectShow ne le reconnaîtront pas comme tels, car ils ne prennent pas en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Une autre approche consiste à écrire votre propre filtre de wrappers DMO qui prend en charge l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
