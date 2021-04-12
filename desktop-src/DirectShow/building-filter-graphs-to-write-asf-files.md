---
description: Création de graphiques de filtre pour écrire des fichiers ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Création de graphiques de filtre pour écrire des fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482272"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="8a4b9-103">Création de graphiques de filtre pour écrire des fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="8a4b9-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="8a4b9-104">Lorsque vous créez du contenu Windows Media, les applications utilisent généralement l’un des scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="8a4b9-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="8a4b9-105">Conversion ou transcodage de contenu d’un autre format au format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="8a4b9-106">Insertion de contenu qui n’est pas basé sur Windows Media (formats de flux natifs) dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="8a4b9-107">Capturer des données actives et les encoder immédiatement dans le format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="8a4b9-108">Transcodage de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="8a4b9-108">Transcoding ASF Files</span></span>

<span data-ttu-id="8a4b9-109">Vous pouvez créer un graphique de filtre de transcodage de fichiers à l’aide du [writer WM ASF](wm-asf-writer-filter.md) de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="8a4b9-110">Le moyen le plus simple consiste à ajouter l’enregistreur WM ASF au graphique de filtre, puis à utiliser la méthode IGraphBuilder :: RenderFile pour générer le graphique automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="8a4b9-111">Une autre méthode consiste à ajouter manuellement chaque filtre au graphique et à connecter les broches.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="8a4b9-112">Après avoir ajouté l’enregistreur ASF WM, configurez-le à l’aide des méthodes IConfigAsfWriter si le profil par défaut n’est pas approprié et connectez les broches d’entrée du writer ASF pour les broches de sortie correspondantes sur les filtres en amont.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="8a4b9-113">L’illustration suivante montre les configurations typiques du graphique de filtre de transcodage WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![graphique de filtre de transcodage](images/asf-transcode.png)

<span data-ttu-id="8a4b9-115">Insertion de formats de flux natifs dans des fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="8a4b9-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="8a4b9-116">Par défaut, le filtre d’enregistreur ASF WM attend des flux audio et vidéo non compressés sur ses broches d’entrée, et utilise les codecs Windows Media Audio et Windows Media Video pour compresser les flux.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="8a4b9-117">Toutefois, le conteneur de fichiers ASF peut être utilisé pour n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="8a4b9-118">En plaçant des données multimédias numériques dans un conteneur de fichiers ASF, vous pouvez ajouter des fonctionnalités fournies par ASF, telles que les métadonnées et la gestion des droits numériques (DRM), sans avoir à transcoder votre contenu.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="8a4b9-119">Pour créer un fichier ASF qui contient du contenu qui n’est pas basé sur un support Windows, l’application doit compresser le flux dans le graphique de filtre en amont de l’enregistreur ASF de WM et contourner le mécanisme de compression du writer ASF en appelant [**IConfigAsfWriter2 :: setParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) , comme suit :</span><span class="sxs-lookup"><span data-stu-id="8a4b9-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="8a4b9-120">Configurez ensuite le filtre avec le profil souhaité.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="8a4b9-121">Il est essentiel que le type de média du flux d’entrée corresponde exactement au format du profil.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="8a4b9-122">Dans certains cas, il peut être nécessaire d’examiner le format du flux d’entrée et de créer un profil personnalisé pour le faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="8a4b9-123">Quand vous connectez l’enregistreur ASF WM au filtre amont, utilisez la méthode IGraphBuilder :: ConnectDirect.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="8a4b9-124">N’utilisez pas de méthodes de « connexion intelligente » comme IGraphBuilder :: Connect ou IGraphBuilder :: RenderFile pour connecter le filtre, car cette opération désactive le mode « contournement de la compression » du filtre.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="8a4b9-125">Capture directe à partir d’un appareil dans un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="8a4b9-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="8a4b9-126">Lorsque vous capturez du contenu audio ou vidéo directement dans un fichier ASF, le graphique de filtre ressemble à ce qui suit, selon le type de périphérique de capture utilisé.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![graphique de capture vidéo Windows Media](images/asf-webcam.png)

<span data-ttu-id="8a4b9-128">Pour plus d’informations sur la création de graphiques de capture vidéo et audio, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a4b9-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="8a4b9-129">Capture audio</span><span class="sxs-lookup"><span data-stu-id="8a4b9-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="8a4b9-130">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8a4b9-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="8a4b9-131">L’enregistreur ASF WM ne s’exécutera pas, sauf si tous ses codes confidentiels sont connectés.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="8a4b9-132">Si vous configurez l’enregistreur WM ASF avec le profil système par défaut (non recommandé), ou un profil avec des flux audio et vidéo, il créera une broche d’entrée pour chaque flux et chacune de ces broches doit être connectée.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="8a4b9-133">Si vous n’envisagez pas de capturer de l’audio, par exemple, assurez-vous de configurer le filtre avec un profil vidéo uniquement afin qu’aucun code confidentiel audio ne soit créé.</span><span class="sxs-lookup"><span data-stu-id="8a4b9-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a4b9-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a4b9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a4b9-135">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a4b9-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



