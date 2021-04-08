---
description: Hébergement direct d’un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hébergement direct d’un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747660"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="5f244-103">Hébergement direct d’un DMO</span><span class="sxs-lookup"><span data-stu-id="5f244-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="5f244-104">Cette section décrit comment une application peut agir en tant que client direct d’un DMO.</span><span class="sxs-lookup"><span data-stu-id="5f244-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="5f244-105">L’application fournit une entrée à la solution DMO, la solution DMO crée une sortie et l’application utilise la sortie pour le rendu, le traitement supplémentaire ou autre chose.</span><span class="sxs-lookup"><span data-stu-id="5f244-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="5f244-106">L’application est responsable des problèmes tels que l’allocation de mémoire, le minutage et la synchronisation et le Threading.</span><span class="sxs-lookup"><span data-stu-id="5f244-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="5f244-107">Ces exigences dépendent de la nature de l’application.</span><span class="sxs-lookup"><span data-stu-id="5f244-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="5f244-108">Les informations contenues dans cette section s’appliquent également si vous écrivez un composant qui agit comme une couche entre une application et un DMO (par exemple, un contrôle ActiveX qui héberge un module DMO).</span><span class="sxs-lookup"><span data-stu-id="5f244-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="5f244-109">En outre, vous devez lire cette section si vous écrivez un DMO, car il décrit les fonctionnalités que votre application DMO doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="5f244-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="5f244-110">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f244-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5f244-111">Définition des types de médias sur un DMO</span><span class="sxs-lookup"><span data-stu-id="5f244-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="5f244-112">Traitement des données dans une DMO</span><span class="sxs-lookup"><span data-stu-id="5f244-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="5f244-113">Traitement sur place</span><span class="sxs-lookup"><span data-stu-id="5f244-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="5f244-114">Flux facultatifs</span><span class="sxs-lookup"><span data-stu-id="5f244-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="5f244-115">Implémentation de IMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="5f244-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="5f244-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f244-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f244-117">Utilisation de DMOs</span><span class="sxs-lookup"><span data-stu-id="5f244-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



