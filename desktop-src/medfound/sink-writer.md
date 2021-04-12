---
description: Le writer du récepteur est un composant permettant d’encoder des fichiers audio ou vidéo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Enregistreur du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318730"
---
# <a name="sink-writer"></a><span data-ttu-id="4418b-103">Enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="4418b-103">Sink Writer</span></span>

<span data-ttu-id="4418b-104">Le writer du récepteur est un composant permettant d’encoder des fichiers audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="4418b-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="4418b-105">Le diagramme suivant montre, à un niveau élevé, comment une application utilise le writer de récepteur pour encoder et fichier audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="4418b-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![diagramme qui montre le writer du récepteur.](images/encoding09.png)

<span data-ttu-id="4418b-107">Le writer du récepteur héberge un récepteur multimédia et éventuellement un ou plusieurs encodeurs.</span><span class="sxs-lookup"><span data-stu-id="4418b-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="4418b-108">Les encodeurs convertissent les données audio ou vidéo non compressées en séquences binaires codées.</span><span class="sxs-lookup"><span data-stu-id="4418b-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="4418b-109">Le récepteur multimédia génère des flux de fichiers binaires dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="4418b-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="4418b-110">L’enregistreur du récepteur effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="4418b-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="4418b-111">Charge le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="4418b-111">Loads the media sink.</span></span>
-   <span data-ttu-id="4418b-112">Recherche et charge les encodeurs.</span><span class="sxs-lookup"><span data-stu-id="4418b-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="4418b-113">Gère le workflow aux encodeurs et au récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="4418b-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="4418b-114">L’application transmet les données audio/vidéo au writer du récepteur en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="4418b-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="4418b-115">La façon dont l’application obtient ou génère les données d’entrée n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="4418b-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="4418b-116">L’une des options consiste à utiliser le [lecteur source](source-reader.md), comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="4418b-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="4418b-117">Toutefois, l’enregistreur du récepteur ne requiert pas l’utilisation du lecteur source.</span><span class="sxs-lookup"><span data-stu-id="4418b-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="4418b-118">Ces deux composants sont indépendants.</span><span class="sxs-lookup"><span data-stu-id="4418b-118">These two components are independent.</span></span>

![diagramme qui montre le lecteur source et le writer du récepteur.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="4418b-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4418b-120">In this section</span></span>

-   [<span data-ttu-id="4418b-121">Utilisation de l’enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="4418b-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="4418b-122">Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo</span><span class="sxs-lookup"><span data-stu-id="4418b-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="4418b-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4418b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4418b-124">Codage et création de fichier</span><span class="sxs-lookup"><span data-stu-id="4418b-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="4418b-125">Vue d’ensemble de l’encodage dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4418b-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



