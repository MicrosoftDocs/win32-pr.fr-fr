---
title: Attributs pour les fichiers vidéo
description: Attributs pour les fichiers vidéo
ms.assetid: 4250ad27-075e-4daa-bc04-d24ddd2e8252
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, fichiers vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd19791857d55be8017d291698a3297b395af550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379725"
---
# <a name="attributes-for-video-files"></a><span data-ttu-id="f74cf-107">Attributs pour les fichiers vidéo</span><span class="sxs-lookup"><span data-stu-id="f74cf-107">Attributes for Video Files</span></span>

<span data-ttu-id="f74cf-108">Cette section répertorie les attributs couramment utilisés pour les fichiers vidéo.</span><span class="sxs-lookup"><span data-stu-id="f74cf-108">This section lists the attributes commonly used for video files.</span></span> <span data-ttu-id="f74cf-109">Nous vous recommandons de définir des attributs pour les fichiers en fonction de ces listes pour vous assurer que vos fichiers sont entièrement compatibles avec une grande variété d’applications de lecture.</span><span class="sxs-lookup"><span data-stu-id="f74cf-109">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="f74cf-110">Les attributs de cette section sont répertoriés en trois catégories : principal, secondaire et tertiaire.</span><span class="sxs-lookup"><span data-stu-id="f74cf-110">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="f74cf-111">Les attributs principaux fournissent les informations les plus élémentaires sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="f74cf-111">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="f74cf-112">Si vous créez des fichiers vidéo pour la distribution, il s’agit de l’ensemble minimal d’attributs que vous devez utiliser.</span><span class="sxs-lookup"><span data-stu-id="f74cf-112">If you are creating video files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="f74cf-113">Les attributs secondaires contiennent des métadonnées communes qui sont importantes mais pas universelles pour tous les fichiers vidéo.</span><span class="sxs-lookup"><span data-stu-id="f74cf-113">Secondary attributes contain common metadata that is important but not universal to all video files.</span></span>

<span data-ttu-id="f74cf-114">Les attributs tertiaires doivent être inclus en fonction des besoins, mais ils ne sont pas essentiels à la description du fichier.</span><span class="sxs-lookup"><span data-stu-id="f74cf-114">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-video"></a><span data-ttu-id="f74cf-115">Attributs principaux pour la vidéo</span><span class="sxs-lookup"><span data-stu-id="f74cf-115">Primary Attributes for Video</span></span>

-   [<span data-ttu-id="f74cf-116">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="f74cf-116">**Author**</span></span>](author.md)
-   [<span data-ttu-id="f74cf-117">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="f74cf-117">**Title**</span></span>](title.md)
-   [<span data-ttu-id="f74cf-118">**WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="f74cf-118">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   <span data-ttu-id="f74cf-119">[**WM/DVDID**](wm-dvdid.md) (s’il est disponible ; sinon, utilisez [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)et [**WM/WMContentID**](wm-wmcontentid.md))</span><span class="sxs-lookup"><span data-stu-id="f74cf-119">[**WM/DVDID**](wm-dvdid.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), and [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="f74cf-120">**WM/genre**</span><span class="sxs-lookup"><span data-stu-id="f74cf-120">**WM/Genre**</span></span>](wm-genre.md)
-   [<span data-ttu-id="f74cf-121">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="f74cf-121">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="f74cf-122">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="f74cf-122">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="f74cf-123">**WM/Provider**</span><span class="sxs-lookup"><span data-stu-id="f74cf-123">**WM/Provider**</span></span>](wm-provider.md)

## <a name="secondary-attributes-for-video"></a><span data-ttu-id="f74cf-124">Attributs secondaires pour la vidéo</span><span class="sxs-lookup"><span data-stu-id="f74cf-124">Secondary Attributes for Video</span></span>

-   [<span data-ttu-id="f74cf-125">**copyright**</span><span class="sxs-lookup"><span data-stu-id="f74cf-125">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="f74cf-126">**WM/composer**</span><span class="sxs-lookup"><span data-stu-id="f74cf-126">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="f74cf-127">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="f74cf-127">**WM/Director**</span></span>](wm-director.md)
-   [<span data-ttu-id="f74cf-128">**WM/EncodingTime**</span><span class="sxs-lookup"><span data-stu-id="f74cf-128">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="f74cf-129">**WM/langage**</span><span class="sxs-lookup"><span data-stu-id="f74cf-129">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="f74cf-130">**WM/ParentalRating**</span><span class="sxs-lookup"><span data-stu-id="f74cf-130">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="f74cf-131">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="f74cf-131">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="f74cf-132">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="f74cf-132">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="f74cf-133">**WM/Toolversion la valeur**</span><span class="sxs-lookup"><span data-stu-id="f74cf-133">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="f74cf-134">**WM/WMCollectionGroupID**</span><span class="sxs-lookup"><span data-stu-id="f74cf-134">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="f74cf-135">**WM/WMCollectionID**</span><span class="sxs-lookup"><span data-stu-id="f74cf-135">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="f74cf-136">**WM/WMContentID**</span><span class="sxs-lookup"><span data-stu-id="f74cf-136">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="f74cf-137">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="f74cf-137">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-video"></a><span data-ttu-id="f74cf-138">Attributs tertiaires pour la vidéo</span><span class="sxs-lookup"><span data-stu-id="f74cf-138">Tertiary Attributes for Video</span></span>

-   [<span data-ttu-id="f74cf-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="f74cf-139">**Description**</span></span>](description.md)
-   [<span data-ttu-id="f74cf-140">**WM/AuthorURL**</span><span class="sxs-lookup"><span data-stu-id="f74cf-140">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="f74cf-141">**WM/conducteur**</span><span class="sxs-lookup"><span data-stu-id="f74cf-141">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="f74cf-142">**WM/ContentGroupDescription**</span><span class="sxs-lookup"><span data-stu-id="f74cf-142">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="f74cf-143">**WM/EncodedBy**</span><span class="sxs-lookup"><span data-stu-id="f74cf-143">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="f74cf-144">**WM/EncodingSettings**</span><span class="sxs-lookup"><span data-stu-id="f74cf-144">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="f74cf-145">**WM/PartOfSet**</span><span class="sxs-lookup"><span data-stu-id="f74cf-145">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="f74cf-146">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="f74cf-146">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="f74cf-147">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="f74cf-147">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="f74cf-148">**WM/serveur de publication**</span><span class="sxs-lookup"><span data-stu-id="f74cf-148">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="f74cf-149">**WM/sous-titre**</span><span class="sxs-lookup"><span data-stu-id="f74cf-149">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="f74cf-150">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="f74cf-150">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="f74cf-151">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="f74cf-151">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="f74cf-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f74cf-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f74cf-153">**Attributs par type**</span><span class="sxs-lookup"><span data-stu-id="f74cf-153">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="f74cf-154">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="f74cf-154">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




