---
title: Insertion de formats de flux natifs dans des fichiers ASF (QASF)
description: Insertion de formats de flux natifs dans des fichiers ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media Format SDK, Native Stream formats (QASF)
- Windows Media Format SDK, insertion de formats de flux natifs dans des fichiers ASF (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), insertion de formats de flux natifs (QASF)
- ASF (format des systèmes avancés), insérer des formats de flux natifs (QASF)
- ASF (Advanced Systems Format), formats de flux natifs (QASF)
- ASF (format des systèmes avancés), formats de flux natifs (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, formats de flux natifs (QASF)
- DirectShow, insertion de formats de flux natifs dans des fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840577"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="21307-118">Insertion de formats de flux natifs dans des fichiers ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="21307-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="21307-119">Par défaut, l' [enregistreur ASF WM](wm-asf-writer-filter.md) attend des flux audio et vidéo non compressés sur ses broches d’entrée, et il utilise le kit de développement logiciel (SDK) du format Windows Media pour accéder aux codecs Windows Media Audio et Windows Media Video, qui compressent les flux.</span><span class="sxs-lookup"><span data-stu-id="21307-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="21307-120">Toutefois, le conteneur de fichiers ASF peut être utilisé pour n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="21307-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="21307-121">En plaçant des données multimédias numériques dans un conteneur de fichiers ASF, vous pouvez ajouter des fonctionnalités fournies par ASF, telles que les métadonnées et la gestion des droits numériques (DRM), sans avoir à transcoder votre contenu.</span><span class="sxs-lookup"><span data-stu-id="21307-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="21307-122">Pour créer un fichier ASF qui contient du contenu qui n’est pas basé sur un support Windows, l’application doit compresser le flux dans le graphique de filtre en amont de l’enregistreur ASF de WM et contourner le mécanisme de compression du writer ASF en appelant [**IConfigAsfWriter2 :: setParam**](iconfigasfwriter2-setparam.md) , comme suit :</span><span class="sxs-lookup"><span data-stu-id="21307-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="21307-123">Configurez ensuite le filtre avec le profil souhaité.</span><span class="sxs-lookup"><span data-stu-id="21307-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="21307-124">Il est essentiel que le type de média du flux d’entrée corresponde exactement au format du profil.</span><span class="sxs-lookup"><span data-stu-id="21307-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="21307-125">Dans certains cas, il peut être nécessaire d’examiner le format du flux d’entrée et de créer un profil personnalisé pour le faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="21307-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="21307-126">Pour plus d’informations, consultez [pour créer des fichiers ASF à l’aide de codecs tiers](to-create-asf-files-using-third-party-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="21307-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="21307-127">Quand vous connectez l’enregistreur ASF WM au filtre amont, utilisez la méthode **IGraphBuilder :: ConnectDirect** .</span><span class="sxs-lookup"><span data-stu-id="21307-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="21307-128">N’utilisez pas de méthodes de « connexion intelligente » comme **IGraphBuilder :: Connect** ou **IGraphBuilder :: RenderFile** pour connecter le filtre, car cette opération désactive le mode « contournement de la compression » du filtre.</span><span class="sxs-lookup"><span data-stu-id="21307-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




