---
description: Prise en charge MPEG-2 dans DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Prise en charge MPEG-2 dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522196"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="df0fd-103">Prise en charge MPEG-2 dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="df0fd-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="df0fd-104">Cette section décrit les composants que vous pouvez utiliser pour lire du contenu MPEG-2 dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="df0fd-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="df0fd-105">Bien que la vidéo DVD soit basée sur MPEG-2, cette section ne décrit pas la lecture ou la navigation sur DVD.</span><span class="sxs-lookup"><span data-stu-id="df0fd-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="df0fd-106">Pour plus d’informations sur les DVD dans DirectShow, consultez [applications DVD](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="df0fd-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="df0fd-107">Les données MPEG-2 peuvent provenir d’un fichier local ou d’une source Live, telle qu’une diffusion réseau ou un appareil D-VHS.</span><span class="sxs-lookup"><span data-stu-id="df0fd-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="df0fd-108">La lecture de fichier est appelée *mode par extraction* , car le filtre de l’analyseur extrait les données du fichier dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="df0fd-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="df0fd-109">Les sources en direct sont appelées *mode Push* , car le filtre source pousse les données dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="df0fd-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="df0fd-110">DirectShow fournit deux filtres qui peuvent analyser les flux système MPEG-2 :</span><span class="sxs-lookup"><span data-stu-id="df0fd-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="df0fd-111">[Démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) (« demux ») : ce filtre prend en charge le mode Push pour les flux de programme et les flux de transport.</span><span class="sxs-lookup"><span data-stu-id="df0fd-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="df0fd-112">Dans Windows XP et versions ultérieures, il prend également en charge le mode par extraction pour les flux de programme.</span><span class="sxs-lookup"><span data-stu-id="df0fd-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="df0fd-113">[Séparateur MPEG-2](mpeg-2-splitter.md): ce filtre prend en charge le mode par extraction pour les flux de programme sur les plateformes de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="df0fd-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="df0fd-114">Ce filtre est déconseillé dans Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="df0fd-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="df0fd-115">Pour utiliser le séparateur MPEG-2 demux ou MPEG-2, vous devez disposer de décodeurs vidéo et audio MPEG-2 compatibles DirectShow acceptant les flux élémentaires (PES).</span><span class="sxs-lookup"><span data-stu-id="df0fd-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="df0fd-116">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="df0fd-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="df0fd-117">Vue d’ensemble des systèmes MPEG-2</span><span class="sxs-lookup"><span data-stu-id="df0fd-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="df0fd-118">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="df0fd-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="df0fd-119">Utilisation du séparateur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="df0fd-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="df0fd-120">Exemples de propriétés MPEG</span><span class="sxs-lookup"><span data-stu-id="df0fd-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="df0fd-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df0fd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df0fd-122">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="df0fd-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



