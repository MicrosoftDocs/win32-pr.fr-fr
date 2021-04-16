---
title: Transcodage de fichiers (QASF)
description: Transcodage de fichiers (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows Media Format SDK, transcodage de fichiers (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), fichiers de transcodage (QASF)
- ASF (format des systèmes avancés), fichiers de transcodage (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, transcodage de fichiers (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551582"
---
# <a name="transcoding-files-qasf"></a><span data-ttu-id="b111c-114">Transcodage de fichiers (QASF)</span><span class="sxs-lookup"><span data-stu-id="b111c-114">Transcoding Files (QASF)</span></span>

<span data-ttu-id="b111c-115">Vous pouvez créer un graphique de filtre de transcodage de fichiers à l’aide du [writer WM ASF](wm-asf-writer-filter.md) de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="b111c-115">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="b111c-116">Le moyen le plus simple consiste à co-créer, à configurer et à ajouter l’enregistreur ASF WM au graphique de filtre, puis à utiliser la méthode **IGraphBuilder :: RenderFile** pour générer le graphique automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b111c-116">The easiest way is to co-create, configure, and add the WM ASF Writer to the filter graph, and then use the **IGraphBuilder::RenderFile** method to build the graph automatically.</span></span>

<span data-ttu-id="b111c-117">Une autre méthode consiste à ajouter manuellement chaque filtre au graphique et à connecter les broches.</span><span class="sxs-lookup"><span data-stu-id="b111c-117">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="b111c-118">Après avoir ajouté l’enregistreur ASF WM, configurez-le à l’aide des méthodes **IConfigAsfWriter** si le profil par défaut n’est pas approprié et connectez les broches d’entrée du writer ASF pour les broches de sortie correspondantes sur les filtres en amont.</span><span class="sxs-lookup"><span data-stu-id="b111c-118">After adding the WM ASF Writer, configure it by using the **IConfigAsfWriter** methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="b111c-119">L’illustration suivante montre les configurations typiques du graphique de filtre de transcodage WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="b111c-119">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![diagrammes de filtre de transcodage standard](images/asf-transcode.png)

 

 




