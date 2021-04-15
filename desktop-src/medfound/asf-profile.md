---
description: Cette rubrique explique comment utiliser des profils ASF dans Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Profil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524660"
---
# <a name="asf-profile"></a><span data-ttu-id="b62e8-103">Profil ASF</span><span class="sxs-lookup"><span data-stu-id="b62e8-103">ASF Profile</span></span>

<span data-ttu-id="b62e8-104">Cette rubrique explique comment utiliser des profils ASF dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b62e8-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="b62e8-105">Un fichier ASF (Advanced Systems Format) contient un ou plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="b62e8-106">Pour chaque flux, l’en-tête ASF contient un en-tête de propriétés de flux qui décrit le flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="b62e8-107">Au niveau de la couche [WMContainer](wmcontainer-asf-components.md) , les objets suivants sont utilisés pour définir ou lire les propriétés des flux ASF :</span><span class="sxs-lookup"><span data-stu-id="b62e8-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="b62e8-108">Objet *Profil ASF* : décrit les flux et leurs relations entre eux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="b62e8-109">L’objet profil ASF expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="b62e8-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="b62e8-110">Objet de *configuration de flux* : décrit un flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="b62e8-111">L’objet de configuration de flux contient un type de média qui décrit le format du flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="b62e8-112">Pour les flux audio et vidéo, le type de média décrit exactement comment le flux est configuré et est utilisé par les codecs qui encodent ou décodent le flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="b62e8-113">L’objet de configuration de flux expose l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="b62e8-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="b62e8-114">Un profil ASF valide contient au moins un objet de configuration de flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="b62e8-115">Objet d' *exclusion mutuelle* : décrit plusieurs flux qui ne sont pas destinés à être lus simultanément.</span><span class="sxs-lookup"><span data-stu-id="b62e8-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="b62e8-116">Un objet d’exclusion mutuelle expose l’interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) .</span><span class="sxs-lookup"><span data-stu-id="b62e8-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="b62e8-117">Un profil ASF contient zéro ou plusieurs objets d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="b62e8-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="b62e8-118">Le diagramme suivant montre la relation entre le profil ASF et les objets contenus dans le profil.</span><span class="sxs-lookup"><span data-stu-id="b62e8-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![diagramme arborescent d’un nœud de profil ASF avec des nœuds enfants de configuration de flux ; le premier point vers le type de média, les deux à l’exclusion mutuelle suivante](images/asf-components02.png)

<span data-ttu-id="b62e8-120">Pour la lecture, le profil ASF est utilisé pour énumérer les flux et rechercher les formats de flux.</span><span class="sxs-lookup"><span data-stu-id="b62e8-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="b62e8-121">Pour l’encodage, le profil ASF est utilisé pour configurer les flux dans le fichier de destination.</span><span class="sxs-lookup"><span data-stu-id="b62e8-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="b62e8-122">Le profil ASF est également utilisé pour configurer le [récepteur de média ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="b62e8-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="b62e8-123">Pour chaque flux du profil ASF, le récepteur multimédia ASF crée un récepteur de flux correspondant.</span><span class="sxs-lookup"><span data-stu-id="b62e8-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b62e8-124">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b62e8-124">In this section</span></span>



| <span data-ttu-id="b62e8-125">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b62e8-125">Topic</span></span>                                                                                           | <span data-ttu-id="b62e8-126">Description</span><span class="sxs-lookup"><span data-stu-id="b62e8-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="b62e8-127">Création d’un profil ASF</span><span class="sxs-lookup"><span data-stu-id="b62e8-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="b62e8-128">Décrit comment créer un objet de profil ASF.</span><span class="sxs-lookup"><span data-stu-id="b62e8-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="b62e8-129">Création et configuration de flux ASF</span><span class="sxs-lookup"><span data-stu-id="b62e8-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="b62e8-130">Décrit comment ajouter des flux à un profil ASF.</span><span class="sxs-lookup"><span data-stu-id="b62e8-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="b62e8-131">Utilisation de l’exclusion mutuelle pour les flux ASF</span><span class="sxs-lookup"><span data-stu-id="b62e8-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="b62e8-132">Décrit comment ajouter des exclusions mutuelles à des flux ASF.</span><span class="sxs-lookup"><span data-stu-id="b62e8-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b62e8-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b62e8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b62e8-134">Types de médias</span><span class="sxs-lookup"><span data-stu-id="b62e8-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="b62e8-135">Didacticiel : 1-passer l’encodage Windows Media</span><span class="sxs-lookup"><span data-stu-id="b62e8-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="b62e8-136">Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR</span><span class="sxs-lookup"><span data-stu-id="b62e8-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="b62e8-137">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="b62e8-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




