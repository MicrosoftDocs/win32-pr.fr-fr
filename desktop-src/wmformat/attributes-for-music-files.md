---
title: Attributs pour les fichiers musicaux
description: Attributs pour les fichiers musicaux
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, fichiers audio
- attributs, fichiers musicaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672045"
---
# <a name="attributes-for-music-files"></a><span data-ttu-id="f3f1c-108">Attributs pour les fichiers musicaux</span><span class="sxs-lookup"><span data-stu-id="f3f1c-108">Attributes for Music Files</span></span>

<span data-ttu-id="f3f1c-109">Cette section répertorie les attributs couramment utilisés pour les fichiers audio contenant de la musique.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-109">This section lists the attributes commonly used for audio files containing music.</span></span> <span data-ttu-id="f3f1c-110">Nous vous recommandons de définir des attributs pour les fichiers en fonction de ces listes pour vous assurer que vos fichiers sont entièrement compatibles avec une grande variété d’applications de lecture.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-110">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="f3f1c-111">Les attributs de cette section sont répertoriés en trois catégories : principal, secondaire et tertiaire.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-111">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="f3f1c-112">Les attributs principaux fournissent les informations les plus élémentaires sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-112">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="f3f1c-113">Si vous créez des fichiers audio pour la distribution, il s’agit de l’ensemble minimal d’attributs que vous devez utiliser.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-113">If you are creating audio files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="f3f1c-114">Les attributs secondaires contiennent des métadonnées communes qui sont importantes mais pas universelles pour tous les fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-114">Secondary attributes contain common metadata that is important but not universal to all audio files.</span></span>

<span data-ttu-id="f3f1c-115">Les attributs tertiaires doivent être inclus en fonction des besoins, mais ils ne sont pas essentiels à la description du fichier.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-115">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-music"></a><span data-ttu-id="f3f1c-116">Attributs principaux pour la musique</span><span class="sxs-lookup"><span data-stu-id="f3f1c-116">Primary Attributes for Music</span></span>

-   [<span data-ttu-id="f3f1c-117">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-117">**Author**</span></span>](author.md)
-   [<span data-ttu-id="f3f1c-118">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-118">**Title**</span></span>](title.md)
-   [<span data-ttu-id="f3f1c-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)
-   [<span data-ttu-id="f3f1c-120">**WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-120">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   [<span data-ttu-id="f3f1c-121">**WM/genre**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-121">**WM/Genre**</span></span>](wm-genre.md)
-   <span data-ttu-id="f3f1c-122">[**WM/MCDI**](wm-mcdi.md) (s’il est disponible ; sinon, utilisez [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)ou [**WM/WMContentID**](wm-wmcontentid.md))</span><span class="sxs-lookup"><span data-stu-id="f3f1c-122">[**WM/MCDI**](wm-mcdi.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), or [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="f3f1c-123">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-123">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="f3f1c-124">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-124">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="f3f1c-125">**WM/Provider**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-125">**WM/Provider**</span></span>](wm-provider.md)
-   [<span data-ttu-id="f3f1c-126">**WM/TrackNumber**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-126">**WM/TrackNumber**</span></span>](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a><span data-ttu-id="f3f1c-127">Attributs secondaires pour la musique</span><span class="sxs-lookup"><span data-stu-id="f3f1c-127">Secondary Attributes for Music</span></span>

-   [<span data-ttu-id="f3f1c-128">**copyright**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-128">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="f3f1c-129">**WM/composer**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-129">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="f3f1c-130">**WM/EncodingTime**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-130">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="f3f1c-131">**WM/langage**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-131">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="f3f1c-132">**WM/ParentalRating**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-132">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="f3f1c-133">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-133">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="f3f1c-134">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-134">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="f3f1c-135">**WM/Toolversion la valeur**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-135">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="f3f1c-136">**WM/WMCollectionGroupID**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-136">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="f3f1c-137">**WM/WMCollectionID**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-137">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="f3f1c-138">**WM/WMContentID**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-138">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="f3f1c-139">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-139">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a><span data-ttu-id="f3f1c-140">Attributs tertiaires pour la musique</span><span class="sxs-lookup"><span data-stu-id="f3f1c-140">Tertiary Attributes for Music</span></span>

-   [<span data-ttu-id="f3f1c-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-141">**Description**</span></span>](description.md)
-   [<span data-ttu-id="f3f1c-142">**WM/AuthorURL**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-142">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="f3f1c-143">**WM/BeatsPerMinute**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-143">**WM/BeatsPerMinute**</span></span>](wm-beatsperminute.md)
-   [<span data-ttu-id="f3f1c-144">**WM/conducteur**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-144">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="f3f1c-145">**WM/ContentGroupDescription**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-145">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="f3f1c-146">**WM/EncodedBy**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-146">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="f3f1c-147">**WM/EncodingSettings**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-147">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="f3f1c-148">**WM/InitialKey**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-148">**WM/InitialKey**</span></span>](wm-initialkey.md)
-   [<span data-ttu-id="f3f1c-149">**WM/paroles**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-149">**WM/Lyrics**</span></span>](wm-lyrics.md)
-   [<span data-ttu-id="f3f1c-150">**Synchronisation des WM et des paroles \_**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-150">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md)
-   [<span data-ttu-id="f3f1c-151">**WM/humeur**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-151">**WM/Mood**</span></span>](wm-mood.md)
-   [<span data-ttu-id="f3f1c-152">**WM/PartOfSet**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-152">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="f3f1c-153">**WM/period**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-153">**WM/Period**</span></span>](wm-period.md)
-   [<span data-ttu-id="f3f1c-154">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-154">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="f3f1c-155">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-155">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="f3f1c-156">**WM/serveur de publication**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-156">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="f3f1c-157">**WM/sous-titre**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-157">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="f3f1c-158">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-158">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="f3f1c-159">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-159">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="f3f1c-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3f1c-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f1c-161">**Attributs par type**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-161">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-162">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-162">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




