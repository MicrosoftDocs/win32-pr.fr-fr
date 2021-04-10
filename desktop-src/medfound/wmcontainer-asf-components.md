---
description: Les objets WMContainer fournissent un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Composants WMContainer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952133"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="e8836-103">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="e8836-103">WMContainer ASF Components</span></span>

<span data-ttu-id="e8836-104">Les objets WMContainer fournissent un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e8836-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="e8836-105">Les [composants ASF de la couche de pipeline](pipeline-layer-asf-components.md) utilisent les objets WMContainer en interne.</span><span class="sxs-lookup"><span data-stu-id="e8836-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="e8836-106">La plupart des applications doivent utiliser les composants de pipeline, plutôt que d’utiliser des objets WMContainer.</span><span class="sxs-lookup"><span data-stu-id="e8836-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="e8836-107">Utilisez WMContainer uniquement si vous avez besoin d’un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="e8836-108">La couche WMContainer comprend les objets suivants :</span><span class="sxs-lookup"><span data-stu-id="e8836-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="e8836-109">Profil ASF</span><span class="sxs-lookup"><span data-stu-id="e8836-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="e8836-110">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="e8836-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="e8836-111">Séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="e8836-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="e8836-112">Multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="e8836-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="e8836-113">Indexeur ASF</span><span class="sxs-lookup"><span data-stu-id="e8836-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="e8836-114">Les rubriques suivantes contiennent des instructions pas à pas sur l’utilisation de WMContainer pour lire ou écrire des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="e8836-115">Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="e8836-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="e8836-116">Didacticiel : copie de flux ASF à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="e8836-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="e8836-117">Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="e8836-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="e8836-118">À propos du conteneur WM</span><span class="sxs-lookup"><span data-stu-id="e8836-118">About WM Container</span></span>

<span data-ttu-id="e8836-119">Les objets WMContainer interagissent directement avec les objets fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="e8836-120">Le diagramme suivant illustre la structure de fichiers ASF et les objets WMContainer correspondants.</span><span class="sxs-lookup"><span data-stu-id="e8836-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![Diagramme montrant la structure des fichiers ASF et les objets Media Foundation correspondants](images/asf-components01.png)

<span data-ttu-id="e8836-122">À l’exception du séparateur et du multiplexeur, chacun de ces objets prend en charge l’analyse (lecture) et l’écriture de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="e8836-123">Le séparateur est utilisé uniquement pour lire des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="e8836-124">Le multiplexeur est utilisé uniquement pour la création de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="e8836-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="e8836-125">Toutes les opérations effectuées par les objets WMContainer sont synchrones, ce qui signifie qu’elles bloquent le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="e8836-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8836-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8836-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8836-127">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8836-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



