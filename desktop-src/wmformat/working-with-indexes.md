---
title: Utilisation des index
description: Utilisation des index
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, index
- ASF (Advanced Systems Format), index
- ASF (format avancé des systèmes), index
- index, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839649"
---
# <a name="working-with-indexes"></a><span data-ttu-id="2b57c-107">Utilisation des index</span><span class="sxs-lookup"><span data-stu-id="2b57c-107">Working with Indexes</span></span>

<span data-ttu-id="2b57c-108">Le kit de développement logiciel (SDK) Windows Media format prend en charge la recherche et la striding de contenu.</span><span class="sxs-lookup"><span data-stu-id="2b57c-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="2b57c-109">La recherche vous permet de spécifier un emplacement dans la chronologie du fichier pour commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="2b57c-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="2b57c-110">Striding vous permet d’avancer rapidement et de rembobiner la sortie d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="2b57c-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="2b57c-111">Les fichiers doivent être indexés pour tirer parti de ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2b57c-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="2b57c-112">Un index est une série de valeurs représentant des positions dans le fichier (heures de présentation, numéros de trame ou codes de temps SMTP) avec des décalages correspondants dans la section de données du fichier pour chaque.</span><span class="sxs-lookup"><span data-stu-id="2b57c-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="2b57c-113">L’indexation est plus importante pour les flux vidéo, car l’heure de présentation du flux audio peut être facilement estimée.</span><span class="sxs-lookup"><span data-stu-id="2b57c-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="2b57c-114">Toutefois, certains flux audio peuvent également nécessiter des index.</span><span class="sxs-lookup"><span data-stu-id="2b57c-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="2b57c-115">Par défaut, le writer indexe chaque nouveau fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2b57c-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="2b57c-116">Si des modifications sont apportées au contenu d’un fichier, vous devez actualiser vous-même l’index à l’aide de l’objet indexeur.</span><span class="sxs-lookup"><span data-stu-id="2b57c-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="2b57c-117">L’indexeur prend en charge l’indexation temporelle et l’indexation basée sur les trames, ainsi que l’indexation basée sur les codes temporels SMPTE (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="2b57c-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="2b57c-118">L’enregistreur crée un index temporel par défaut pour chaque nouveau flux vidéo encodé dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="2b57c-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="2b57c-119">Vous devez explicitement configurer et appeler l’indexeur pour créer un index de code de temps basé sur des trames ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2b57c-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="2b57c-120">Lorsque des modifications sont apportées au contenu d’un fichier ASF, elles doivent être réindexées.</span><span class="sxs-lookup"><span data-stu-id="2b57c-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="2b57c-121">Les sections suivantes présentent un exemple de code pour l’exécution de tâches d’indexation courantes.</span><span class="sxs-lookup"><span data-stu-id="2b57c-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="2b57c-122">Pour désactiver l’indexation automatique</span><span class="sxs-lookup"><span data-stu-id="2b57c-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="2b57c-123">Pour configurer l’indexeur</span><span class="sxs-lookup"><span data-stu-id="2b57c-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="2b57c-124">Pour indexer un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="2b57c-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="2b57c-125">Pour arrêter l’indexation en cours</span><span class="sxs-lookup"><span data-stu-id="2b57c-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="2b57c-126">En outre, l’exemple d’application DSCopy illustre l’utilisation de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="2b57c-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="2b57c-127">Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2b57c-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




