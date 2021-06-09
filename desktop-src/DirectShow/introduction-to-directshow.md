---
description: Présentation de DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Présentation de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827223"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="417ff-103">Présentation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="417ff-103">Introduction to DirectShow</span></span>

<span data-ttu-id="417ff-104">Microsoft® DirectShow® est une architecture de diffusion multimédia en continu sur la plateforme Microsoft Windows®.</span><span class="sxs-lookup"><span data-stu-id="417ff-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="417ff-105">DirectShow offre une capture et une lecture de grande qualité des flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="417ff-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="417ff-106">Il prend en charge une grande variété de formats, notamment les fichiers ASF (Advanced Systems Format), MPEG (motion image experts Group), AVI (Audio-Video entrelacé), MPEG Audio Layer-3 (MP3) et les fichiers audio WAV.</span><span class="sxs-lookup"><span data-stu-id="417ff-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="417ff-107">Il prend en charge la capture à partir d’appareils numériques et analogiques basés sur le Windows Driver Model (WDM) ou vidéo pour Windows.</span><span class="sxs-lookup"><span data-stu-id="417ff-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="417ff-108">Il détecte et utilise automatiquement le matériel d’accélération vidéo et audio lorsqu’il est disponible, mais il prend également en charge les systèmes sans accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="417ff-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="417ff-109">DirectShow est basé sur le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="417ff-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="417ff-110">Pour écrire une application ou un composant DirectShow, vous devez comprendre la programmation du client COM.</span><span class="sxs-lookup"><span data-stu-id="417ff-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="417ff-111">Pour la plupart des applications, il n’est pas nécessaire d’implémenter vos propres objets COM.</span><span class="sxs-lookup"><span data-stu-id="417ff-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="417ff-112">DirectShow fournit les composants dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="417ff-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="417ff-113">Toutefois, si vous souhaitez étendre DirectShow en écrivant vos propres composants, vous devez les implémenter en tant qu’objets COM.</span><span class="sxs-lookup"><span data-stu-id="417ff-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="417ff-114">DirectShow est conçu pour C++.</span><span class="sxs-lookup"><span data-stu-id="417ff-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="417ff-115">Microsoft ne fournit pas d’API gérée pour DirectShow.</span><span class="sxs-lookup"><span data-stu-id="417ff-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="417ff-116">DirectShow simplifie la lecture du média, la conversion de format et les tâches de capture.</span><span class="sxs-lookup"><span data-stu-id="417ff-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="417ff-117">En même temps, il fournit l’accès à l’architecture du contrôle de flux sous-jacent pour les applications qui nécessitent des solutions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="417ff-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="417ff-118">Vous pouvez également créer vos propres composants DirectShow pour prendre en charge de nouveaux formats ou des effets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="417ff-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="417ff-119">Parmi les types d’applications que vous pouvez écrire avec DirectShow, citons les lecteurs de fichiers, les lecteurs TV et DVD, les applications de modification vidéo, les convertisseurs de format de fichier, les applications de capture audio-video, les encodeurs et les décodeurs, les processeurs de signal numérique, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="417ff-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="417ff-120">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="417ff-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="417ff-121">Nouveautés de DirectShow</span><span class="sxs-lookup"><span data-stu-id="417ff-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="417ff-122">Formats pris en charge dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="417ff-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="417ff-123">FAQ DirectShow</span><span class="sxs-lookup"><span data-stu-id="417ff-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="417ff-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="417ff-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="417ff-125">Prise en main</span><span class="sxs-lookup"><span data-stu-id="417ff-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="417ff-126">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="417ff-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



