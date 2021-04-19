---
title: Fonctionnalités des fichiers ASF
description: Fonctionnalités des fichiers ASF
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- SDK Windows Media format, fonctionnalités de fichier ASF
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- ASF (Advanced Systems Format), fonctionnalités de fichier
- ASF (format de systèmes avancés), fonctionnalités de fichier
- ASF (Advanced Systems Format), fonctionnalités
- ASF (format des systèmes avancés), fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106510502"
---
# <a name="asf-file-features"></a><span data-ttu-id="ce0a0-109">Fonctionnalités des fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="ce0a0-109">ASF File Features</span></span>

<span data-ttu-id="ce0a0-110">L’objectif principal du kit de développement logiciel (SDK) du format Windows Media est de fournir la prise en charge de l’encapsulation des données multimédias numériques dans des fichiers ASF (Advanced Systems Format) et de la fourniture des médias à une application cliente.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="ce0a0-111">Les scénarios de remise peuvent varier considérablement d’une application à l’autre, tout en utilisant la structure de fichiers ASF entre la création et la remise.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="ce0a0-112">Les fichiers ASF sont conformes à une structure bien définie mais très flexible.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="ce0a0-113">Pour plus d’informations sur la structure des fichiers ASF, consultez [vue d’ensemble du format ASF](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="ce0a0-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="ce0a0-114">Des informations détaillées sur les données contenues dans un fichier ASF sont fournies dans la spécification ASF, que vous pouvez télécharger à partir du [site Web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span><span class="sxs-lookup"><span data-stu-id="ce0a0-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="ce0a0-115">Le kit de développement logiciel (SDK) Windows Media format prend en charge les fonctionnalités de la spécification ASF principalement par le biais du profil utilisé pour créer un fichier.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="ce0a0-116">Pour plus d’informations sur les profils, consultez [profils](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ce0a0-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="ce0a0-117">Les fonctionnalités suivantes sont présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="ce0a0-118">Flux audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="ce0a0-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="ce0a0-119">Flux d’images</span><span class="sxs-lookup"><span data-stu-id="ce0a0-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="ce0a0-120">Flux arbitraires</span><span class="sxs-lookup"><span data-stu-id="ce0a0-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="ce0a0-121">Commandes de script</span><span class="sxs-lookup"><span data-stu-id="ce0a0-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="ce0a0-122">Extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="ce0a0-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="ce0a0-123">Prise en charge des codes temporels SMPTE</span><span class="sxs-lookup"><span data-stu-id="ce0a0-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="ce0a0-124">Exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="ce0a0-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="ce0a0-125">Hiérarchisation des flux</span><span class="sxs-lookup"><span data-stu-id="ce0a0-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="ce0a0-126">Partage de bande passante</span><span class="sxs-lookup"><span data-stu-id="ce0a0-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="ce0a0-127">Index</span><span class="sxs-lookup"><span data-stu-id="ce0a0-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="ce0a0-128">Marqueurs</span><span class="sxs-lookup"><span data-stu-id="ce0a0-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="ce0a0-129">Réponse du lecteur aux fonctionnalités ASF</span><span class="sxs-lookup"><span data-stu-id="ce0a0-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="ce0a0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce0a0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce0a0-131">**Fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="ce0a0-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




