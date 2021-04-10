---
description: Avantages de DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Avantages de DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200802"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="c499f-103">Avantages de DMOs</span><span class="sxs-lookup"><span data-stu-id="c499f-103">Benefits of DMOs</span></span>

<span data-ttu-id="c499f-104">DMOs offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="c499f-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="c499f-105">Elles sont généralement plus petites et plus simples que les filtres DirectShow, car elles prennent en charge moins de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c499f-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="c499f-106">Elles sont plus flexibles que les filtres DirectShow, car elles ne nécessitent pas de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c499f-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="c499f-107">Vous pouvez les utiliser avec DirectShow lorsque vous avez besoin des services fournis par DirectShow, tels que la synchronisation, la connexion intelligente, le traitement automatique du workflow de données et la gestion des threads.</span><span class="sxs-lookup"><span data-stu-id="c499f-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="c499f-108">Les clients qui n’ont pas besoin de ces services peuvent accéder directement à DMOs.</span><span class="sxs-lookup"><span data-stu-id="c499f-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="c499f-109">DMOs effectue toujours le traitement synchrone des données, ce qui élimine la plupart des problèmes de thread que vous devez prendre en compte si vous écrivez un filtre.</span><span class="sxs-lookup"><span data-stu-id="c499f-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="c499f-110">Contrairement aux codecs ACM et VCM traditionnels, les DMOs sont basés sur le modèle COM (Component Object Model), de sorte qu’ils peuvent être étendus via **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c499f-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="c499f-111">DMOs prennent en charge un modèle de diffusion en continu plus généralisé que les codecs ACM ou VCM.</span><span class="sxs-lookup"><span data-stu-id="c499f-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="c499f-112">À l’instar des filtres DirectShow, DMOs peut prendre en charge plusieurs entrées et sorties.</span><span class="sxs-lookup"><span data-stu-id="c499f-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="c499f-113">Pour ces raisons, DMOs est maintenant recommandé comme solution pour écrire des encodeurs, des décodeurs et des effets audio.</span><span class="sxs-lookup"><span data-stu-id="c499f-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="c499f-114">De nombreux autres scénarios sont également possibles, selon les besoins de l’application.</span><span class="sxs-lookup"><span data-stu-id="c499f-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="c499f-115">Différences entre les DMOs et les filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="c499f-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="c499f-116">Les filtres DirectShow ne peuvent pas fonctionner en dehors d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c499f-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="c499f-117">Dans DirectShow, le gestionnaire de graphique de filtre entre l’application et les filtres.</span><span class="sxs-lookup"><span data-stu-id="c499f-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="c499f-118">Les filtres DirectShow effectuent la majeure partie du travail nécessaire pour diffuser des données en continu, notamment :</span><span class="sxs-lookup"><span data-stu-id="c499f-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="c499f-119">Allocation des tampons.</span><span class="sxs-lookup"><span data-stu-id="c499f-119">Allocating buffers.</span></span>
-   <span data-ttu-id="c499f-120">Négociation des types de médias et des connexions à d’autres filtres.</span><span class="sxs-lookup"><span data-stu-id="c499f-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="c499f-121">Transmission de données via le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c499f-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="c499f-122">Envoi d’événements au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c499f-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="c499f-123">Synchronisation de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="c499f-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="c499f-124">En revanche, DMO n’effectue aucune de ces opérations.</span><span class="sxs-lookup"><span data-stu-id="c499f-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="c499f-125">Au lieu de cela, ces types de tâches sont la responsabilité du client à l’aide d’DMO.</span><span class="sxs-lookup"><span data-stu-id="c499f-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="c499f-126">Le client alloue des tampons, les remplit avec les données et les remet à la solution DMO.</span><span class="sxs-lookup"><span data-stu-id="c499f-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="c499f-127">DMO traite les données et le client récupère les tampons de sortie résultants.</span><span class="sxs-lookup"><span data-stu-id="c499f-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c499f-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c499f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c499f-129">À propos de DMOs</span><span class="sxs-lookup"><span data-stu-id="c499f-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



