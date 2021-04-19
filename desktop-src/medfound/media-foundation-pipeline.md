---
description: La couche de pipeline dans Microsoft Media Foundation est la couche de l’architecture qui génère ou traite directement les données multimédias.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Pipeline Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539379"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="90ff0-103">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90ff0-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="90ff0-104">La couche de *pipeline* dans Microsoft Media Foundation est la couche de l’architecture qui génère ou traite directement les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="90ff0-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="90ff0-105">La plupart des applications n’appellent pas directement des méthodes sur les composants de pipeline, bien qu’il soit possible de le faire.</span><span class="sxs-lookup"><span data-stu-id="90ff0-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="90ff0-106">Lisez ces rubriques si vous écrivez un composant de pipeline personnalisé.</span><span class="sxs-lookup"><span data-stu-id="90ff0-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="90ff0-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="90ff0-107">In this section</span></span>



| <span data-ttu-id="90ff0-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="90ff0-108">Topic</span></span>                                                                     | <span data-ttu-id="90ff0-109">Description</span><span class="sxs-lookup"><span data-stu-id="90ff0-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ff0-110">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="90ff0-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="90ff0-111">Les sources multimédias génèrent des données multimédias, généralement à partir d’un fichier, d’un périphérique de capture ou d’un flux réseau.</span><span class="sxs-lookup"><span data-stu-id="90ff0-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="90ff0-112">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90ff0-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="90ff0-113">Media Foundation transforme les données du support de traitement (MFTs).</span><span class="sxs-lookup"><span data-stu-id="90ff0-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="90ff0-114">Par exemple, les codecs dans Media Foundation sont implémentés en tant que MFTs.</span><span class="sxs-lookup"><span data-stu-id="90ff0-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="90ff0-115">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="90ff0-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="90ff0-116">Les récepteurs multimédias consomment des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="90ff0-116">Media sinks consume media data.</span></span> <span data-ttu-id="90ff0-117">Par exemple, un récepteur multimédia peut écrire les données dans un fichier ou envoyer les données sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="90ff0-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="90ff0-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90ff0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ff0-119">Media Foundation et COM</span><span class="sxs-lookup"><span data-stu-id="90ff0-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="90ff0-120">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90ff0-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




