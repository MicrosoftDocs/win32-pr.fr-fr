---
description: Dans le modèle de pipeline Media Foundations, une source de média est connectée à une transformation qui est encore connectée à un récepteur multimédia.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Composants ASF de couche de pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529137"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="ae009-103">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="ae009-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="ae009-104">Dans le modèle de pipeline d’Media Foundation, une source de média est connectée à une transformation qui est encore connectée à un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae009-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="ae009-105">Les données contenues dans la source circulent dans la transformation et génèrent des échantillons de média de sortie dans le récepteur à des fins de lecture ou d’encodage.</span><span class="sxs-lookup"><span data-stu-id="ae009-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="ae009-106">Selon que l’application souhaite lire du contenu ASF ou Encoder dans un fichier ASF, l’application doit générer le pipeline différemment.</span><span class="sxs-lookup"><span data-stu-id="ae009-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="ae009-107">Les rubriques suivantes contiennent des informations sur les composants de la couche de pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae009-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="ae009-108">Source de média ASF</span><span class="sxs-lookup"><span data-stu-id="ae009-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="ae009-109">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="ae009-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="ae009-110">Récepteurs de média ASF</span><span class="sxs-lookup"><span data-stu-id="ae009-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="ae009-111">Les trois principaux composants d’un pipeline ASF pour la lecture sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ae009-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="ae009-112">La source du média ASF est fournie par Media Foundation qui représente un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="ae009-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="ae009-113">Rééchantillonneurs audio, redimensionnements d’images vidéo, etc., (transformation)</span><span class="sxs-lookup"><span data-stu-id="ae009-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="ae009-114">Convertisseur audio et vidéo (récepteurs)</span><span class="sxs-lookup"><span data-stu-id="ae009-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="ae009-115">Pour plus d’informations sur la création d’un pipeline de lecture, consultez [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="ae009-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="ae009-116">Les trois principaux composants d’un pipeline ASF pour l’encodage sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ae009-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="ae009-117">Source de média représentant les données dans un format qui doit être converti.</span><span class="sxs-lookup"><span data-stu-id="ae009-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="ae009-118">Ce composant peut être l’une des sources de média par défaut fournies par Media Foundation ou une source personnalisée qui expose l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="ae009-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="ae009-119">Encodeurs Windows Media (transformation) qui effectuent la conversion de format.</span><span class="sxs-lookup"><span data-stu-id="ae009-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="ae009-120">Récepteurs de média ASF fournis par Media Foundation qui écrivent des objets ASF et des exemples de média dans un fichier de sortie spécifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="ae009-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="ae009-121">Le pipeline est représenté dans une topologie et chaque objet dans le pipeline est représenté par un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="ae009-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="ae009-122">Pour la lecture et l’encodage, toutes les opérations de pipeline sont gérées par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae009-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="ae009-123">L’une des responsabilités de la session multimédia est de s’assurer que le pipeline dispose de tous les composants requis pour générer la sortie.</span><span class="sxs-lookup"><span data-stu-id="ae009-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="ae009-124">Par exemple, dans un pipeline d’encodage, si le format de la source audio est différent du format cible, la session multimédia insère des composants de transformation supplémentaires, tels que le rééchantillonneur qui effectue des conversions de taux d’échantillonnage appropriées.</span><span class="sxs-lookup"><span data-stu-id="ae009-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="ae009-125">Le contrôle de workflow via le pipeline est également géré par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae009-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="ae009-126">Dans un scénario de lecture, démarrant la session multimédia, la session multimédia envoie des exemples à SAR et EVR, qui les affiche sur le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae009-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="ae009-127">Pour l’encodage, le démarrage de la session multimédia commence le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="ae009-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="ae009-128">La session avertit de façon asynchrone l’application lorsque l’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="ae009-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="ae009-129">La rubrique suivante contient des instructions pas à pas sur l’utilisation des composants de couche de pipeline pour créer une topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="ae009-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="ae009-130">composants pour la lecture et l’écriture de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="ae009-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="ae009-131">Didacticiel : 1-passer l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="ae009-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="ae009-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae009-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae009-133">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae009-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



