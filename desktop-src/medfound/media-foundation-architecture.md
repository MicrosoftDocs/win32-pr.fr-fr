---
description: Cette section décrit la conception générale de Microsoft Media Foundation. Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez Media Foundation Guide de programmation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Architecture Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106544382"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="f698d-104">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-104">Media Foundation Architecture</span></span>

<span data-ttu-id="f698d-105">Cette section décrit la conception générale de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f698d-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="f698d-106">Pour plus d’informations sur l’utilisation de Media Foundation pour des tâches de programmation spécifiques, consultez [Media Foundation Guide de programmation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="f698d-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f698d-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f698d-107">In this section</span></span>



| <span data-ttu-id="f698d-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f698d-108">Topic</span></span>                                                                                                         | <span data-ttu-id="f698d-109">Description</span><span class="sxs-lookup"><span data-stu-id="f698d-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f698d-110">Vue d’ensemble de l’architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="f698d-111">Offre une vue d’ensemble de l’architecture Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f698d-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="f698d-112">Primitives de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="f698d-113">Décrit certaines interfaces de base utilisées dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f698d-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="f698d-114">Presque toutes les applications de Media Foundation utilisent ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="f698d-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="f698d-115">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="f698d-116">Décrit les fonctions de Media Foundation principales, telles que les rappels asynchrones et les files d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="f698d-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="f698d-117">Certaines applications peuvent utiliser des interfaces de niveau plateforme.</span><span class="sxs-lookup"><span data-stu-id="f698d-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="f698d-118">En outre, les plug-ins personnalisés, tels que les sources multimédias et MFTs, utilisent ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="f698d-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="f698d-119">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="f698d-120">La couche de pipeline Media Foundation se compose de sources multimédias, de MFTs et de récepteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="f698d-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="f698d-121">La plupart des applications n’appellent pas directement des méthodes sur la couche de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f698d-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="f698d-122">Au lieu de cela, les applications utilisent l’une des couches supérieures, telles que la session multimédia ou le lecteur source et le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="f698d-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="f698d-123">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="f698d-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="f698d-124">La session multimédia gère le workflow de données dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f698d-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="f698d-125">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="f698d-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="f698d-126">Le lecteur source permet à une application d’obtenir des données à partir d’une source multimédia, sans que les applicating aient besoin d’appeler directement les API de source de média.</span><span class="sxs-lookup"><span data-stu-id="f698d-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="f698d-127">Le lecteur source peut également effectuer le décodage des flux compressés.</span><span class="sxs-lookup"><span data-stu-id="f698d-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="f698d-128">Chemin du média protégé</span><span class="sxs-lookup"><span data-stu-id="f698d-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="f698d-129">Le chemin d’accès au média protégé (PMP) fournit un environnement protégé pour la diffusion de contenu vidéo Premium.</span><span class="sxs-lookup"><span data-stu-id="f698d-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="f698d-130">Il n’est pas nécessaire d’utiliser l’PMP lors de l’écriture d’une application Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f698d-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f698d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f698d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f698d-132">À propos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="f698d-133">Media Foundation : notions essentielles</span><span class="sxs-lookup"><span data-stu-id="f698d-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="f698d-134">Media Foundation et COM</span><span class="sxs-lookup"><span data-stu-id="f698d-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="f698d-135">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f698d-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




