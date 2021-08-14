---
description: Création de graphiques de filtre pour écrire des fichiers ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Création de graphiques de filtre pour écrire des fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe53dcee310be34c321dfc2e988807184735a24b0793d68e3ca7dea10d0b29e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662745"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Création de graphiques de filtre pour écrire des fichiers ASF

lorsque vous créez Windows contenu multimédia, les applications utilisent généralement l’un des scénarios suivants :

-   conversion ou transcodage de contenu d’un autre format en Windows format multimédia.
-   insertion de contenu qui n’est pas Windows des fichiers multimédias (formats de flux natifs) dans des fichiers ASF.
-   capturer des données actives et les encoder immédiatement dans Windows Format multimédia.

Transcodage de fichiers ASF

Vous pouvez créer un graphique de filtre de transcodage de fichiers à l’aide du [writer WM ASF](wm-asf-writer-filter.md) de différentes façons. Le moyen le plus simple consiste à ajouter l’enregistreur WM ASF au graphique de filtre, puis à utiliser la méthode IGraphBuilder :: RenderFile pour générer le graphique automatiquement.

Une autre méthode consiste à ajouter manuellement chaque filtre au graphique et à connecter les broches. Après avoir ajouté l’enregistreur ASF WM, configurez-le à l’aide des méthodes IConfigAsfWriter si le profil par défaut n’est pas approprié et connectez les broches d’entrée du writer ASF pour les broches de sortie correspondantes sur les filtres en amont.

L’illustration suivante montre les configurations typiques du graphique de filtre de transcodage WM ASF Writer.

![graphique de filtre de transcodage](images/asf-transcode.png)

Insertion de formats de flux natifs dans des fichiers ASF

par défaut, le filtre d’enregistreur ASF WM attend des flux audio et vidéo non compressés sur ses broches d’entrée, et utilise les codecs Windows Media Audio et Windows Media Video pour compresser les flux. Toutefois, le conteneur de fichiers ASF peut être utilisé pour n’importe quel type de données. En plaçant des données multimédias numériques dans un conteneur de fichiers ASF, vous pouvez ajouter des fonctionnalités fournies par ASF, telles que les métadonnées et la gestion des droits numériques (DRM), sans avoir à transcoder votre contenu.

pour créer un fichier ASF qui contient du contenu qui n’est pas Windows support, l’application doit compresser le flux dans le graphique de filtre en amont de l’enregistreur asf de wm et contourner le mécanisme de compression du writer asf en appelant [**IConfigAsfWriter2 :: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) , comme suit :


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Configurez ensuite le filtre avec le profil souhaité. Il est essentiel que le type de média du flux d’entrée corresponde exactement au format du profil. Dans certains cas, il peut être nécessaire d’examiner le format du flux d’entrée et de créer un profil personnalisé pour le faire correspondre.

Quand vous connectez l’enregistreur ASF WM au filtre amont, utilisez la méthode IGraphBuilder :: ConnectDirect. n’utilisez pas de méthodes de « connexion intelligente » comme IGraphBuilder :: Connecter ou IGraphBuilder :: RenderFile pour connecter le filtre, car cette opération désactive le mode « contournement de la compression » du filtre.

Capture directe à partir d’un appareil dans un fichier ASF

Lorsque vous capturez du contenu audio ou vidéo directement dans un fichier ASF, le graphique de filtre ressemble à ce qui suit, selon le type de périphérique de capture utilisé.

![graphique de capture vidéo Windows Media](images/asf-webcam.png)

Pour plus d’informations sur la création de graphiques de capture vidéo et audio, consultez les rubriques suivantes :

-   [Capture audio](audio-capture.md)
-   [Capture vidéo](video-capture.md)

L’enregistreur ASF WM ne s’exécutera pas, sauf si tous ses codes confidentiels sont connectés. Si vous configurez l’enregistreur WM ASF avec le profil système par défaut (non recommandé), ou un profil avec des flux audio et vidéo, il créera une broche d’entrée pour chaque flux et chacune de ces broches doit être connectée. Si vous n’envisagez pas de capturer de l’audio, par exemple, assurez-vous de configurer le filtre avec un profil vidéo uniquement afin qu’aucun code confidentiel audio ne soit créé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



