---
description: Utilisation des codecs de média de fenêtre dans DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Utilisation des codecs de média de fenêtre dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313641"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Utilisation des codecs de média de fenêtre dans DirectShow

les objets d’encodeur et de décodeur Windows Media Audio et vidéo ont été initialement conçus et optimisés pour fonctionner avec le format de conteneur de fichiers ASF et le kit de développement logiciel (SDK) Windows Media format. les objets codec fonctionnent bien dans DirectShow pour certains scénarios, à savoir un encodage CBR et un encodage VBR basé sur la qualité des flux vidéo. toutefois, si vous envisagez d’utiliser les objets codec directement dans DirectShow à l’aide de conteneurs de fichiers autres que ASF, vous devez connaître à l’avance certains comportements et problèmes.

> [!Note]  
> si vous envisagez d’utiliser des codecs autonomes avec DirectShow, vous souhaiterez probablement les utiliser en tant que DMOs uniquement. En d’autres termes, vous allez utiliser l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) au lieu de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Fichier audio WM dans les fichiers AVI

vous pouvez utiliser DirectShow pour encoder des flux WMA dans n’importe quel format de conteneur de fichiers pour lequel vous avez un filtre multiplexeur. toutefois, les interfaces de codec vidéo et Windows Media Audio ne prennent pas en charge WMA dans les fichiers avi, car il est impossible d’utiliser les filtres de lecture avi DirectShow par défaut pour maintenir la synchronisation Audio-vidéo dans un fichier AVI avec un flux WMA. Pour plus d’informations, consultez [stockage de médias compressés dans des fichiers AVI](storingcompressedmediainavifiles.md).

l’encodeur audio DMO génère des échantillons de durée variable, même en mode « taux binaire constant ». Cela fonctionne donc mieux avec les formats de conteneur de fichiers qui utilisent des horodatages. Les fichiers AVI ne fournissent pas d’horodatage pour chaque exemple audio ou groupe d’exemples. dans DirectShow, le filtre de séparateur AVI fabrique des horodatages pour chaque groupe d’échantillons (chaque bloc audio) en fonction de la valeur **nAvgBytesPerSec** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dans l’en-tête de flux AVI.

L’hypothèse sous-jacente à ce calcul est que tous les échantillons audio dans le flux sont de même durée ; toutefois, les résultats de la DMO ne sont pas de la même durée et les horodatages appliqués par le séparateur AVI ne sont pas exacts. par conséquent, il n’est pas possible, sans modifier le séparateur AVI ou le décodeur audio DMO, d’utiliser n’importe quelle application basée sur DirectShow pour lire des fichiers avi avec des flux audio et vidéo synchronisés. le codec vocal Windows Media Audio 9 fonctionne dans certains cas, mais même si cela perd la synchronisation après toute opération de recherche, il ne peut pas être considéré comme une solution viable.

Si vous disposez d’un encodeur MP3, vous pouvez créer des fichiers AVI avec WMV et MP3 pour le flux audio. ces fichiers sont lus et recherchent correctement dans Lecteur Windows Media et d’autres applications basées sur DirectShow, car le séparateur AVI contient du code de gestion spécial pour les flux MP3. Une autre option consiste à utiliser l’audio PCM non compressé, bien que la taille du fichier résultant soit nettement supérieure à celle d’un flux audio compressé. étant donné que l’exemple d’application DirectShow crée des fichiers AVI, il ne montre pas comment utiliser l’encodeur audio DMO.

## <a name="one-pass-encoding"></a>Encodage à passage unique

l’encodeur vidéo DMO fonctionne facilement dans DirectShow pour deux modes d’encodage : CBR et VBR basés sur la qualité. Tant que vous suivez l’ordre correct des opérations lors de la génération du graphique de filtre, comme illustré dans l’exemple d’application, il est relativement simple de placer du contenu WMV dans un fichier AVI à l’aide du multiplexeur AVI et du writer de fichier.

## <a name="two-pass-encoding"></a>Encodage en deux passes

les modes d’encodage en deux passes nécessitent une approche plus complexe de la génération et de la diffusion de graphiques pour empêcher le DMO de vider son contenu à partir de la première passe avant de commencer la deuxième passe. dans l’encodage en deux passes, il est nécessaire d’exécuter le graphique une seule fois pour que le DMO puisse effectuer son analyse de prétraitement des données de fichier, puis rembobiner le graphique et l’exécuter de nouveau afin que le DMO puisse effectuer l’encodage réel.

lorsque le graphique passe à l’état d’exécution pour la deuxième passe, le Wrapper DMO définit l’indicateur de discontinuité sur le premier exemple, car l’horodatage n’est pas séquentiel avec le dernier horodatage sur la première passe. lorsque le DMO, qui n’a pas été conçu pour fonctionner dans DirectShow de cette manière, reçoit l’indicateur de discontinuité, il effectue un vidage et perd les données stockées à partir de la première passe. pour contourner ce problème, la meilleure solution consiste probablement à écrire un filtre de Wrapper DMO personnalisé qui ne définit pas l’indicateur de discontinuité lorsque le graphique est cherché après le premier passage. l’exemple Video for Windows (VfW) dans ce kit de développement logiciel (SDK) montre comment effectuer un encodage en deux passes.

## <a name="interlaced-content"></a>Contenu entrelacé

l’encodeur WMV DMO peut encoder du contenu entrelacé tout en préservant l’entrelacement, ce qui est utile pour le contenu capturé à partir d’un téléviseur et peut également être lu sur un téléviseur. toutefois, il n’est pas possible de conserver l’entrelacement à l’aide du Wrapper DMO par défaut, car ce filtre ne prend pas en charge [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) sur ses exemples d’entrée.

le DMO utilise cette interface pour obtenir les paramètres entrelacés pour chaque échantillon qu’il reçoit. si l’interface est introuvable, comme c’est le cas avec le Wrapper DMO, le DMO traite simplement les exemples d’entrée comme non entrelacés. pour effectuer un encodage entrelacé dans DirectShow, il existe plusieurs alternatives. l’approche la plus simple consiste à utiliser le kit de développement logiciel (SDK) de la série 9 Windows Media Format 9 directement ou à l’aide du filtre de DirectShow du Writer WM pour créer un fichier asf entrelacé. Vous pouvez ensuite transcoder ce fichier dans un autre format. si vous transcodez dans AVI, vous disposerez d’un fichier entrelacé, mais les filtres de lecture DirectShow AVI standard ne le reconnaîtront pas comme tels, car ils ne prennent pas en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). une autre approche consiste à écrire votre propre filtre de Wrapper DMO qui prend en charge l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
