---
title: Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media format 11)
description: En savoir plus sur les attributs avec plusieurs valeurs dans le kit de développement logiciel (SDK) Windows Media format 11. Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, valeurs multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262691"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="5ee34-108">Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="5ee34-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5ee34-109">Plusieurs valeurs peuvent être assignées à certains des attributs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="5ee34-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="5ee34-110">Par exemple, **Artist** est un attribut qui peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="5ee34-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="5ee34-111">Vous pouvez appeler [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) plusieurs fois pour ajouter autant de valeurs d' **artistes** que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5ee34-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="5ee34-112">Si vous effectuez plusieurs appels à **AddAttribute** pour les attributs qui ne prennent pas en charge plusieurs valeurs, la méthode peut retourner un code d’erreur ou ignorer simplement votre demande.</span><span class="sxs-lookup"><span data-stu-id="5ee34-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="5ee34-113">Le tableau suivant répertorie les attributs qui prennent en charge plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="5ee34-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="5ee34-114">Certains attributs peuvent avoir plusieurs valeurs uniquement dans des fichiers ASF, tandis que d’autres peuvent avoir plusieurs valeurs dans des fichiers ASF et MP3.</span><span class="sxs-lookup"><span data-stu-id="5ee34-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="5ee34-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ee34-115">Attribute</span></span>                                                 | <span data-ttu-id="5ee34-116">Prise en charge de plusieurs valeurs</span><span class="sxs-lookup"><span data-stu-id="5ee34-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="5ee34-117">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="5ee34-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="5ee34-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-119">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="5ee34-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="5ee34-120">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-120">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-121">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="5ee34-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="5ee34-122">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-122">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-123">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="5ee34-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="5ee34-124">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-124">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-125">**WM/composer**</span><span class="sxs-lookup"><span data-stu-id="5ee34-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="5ee34-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-127">**WM/conducteur**</span><span class="sxs-lookup"><span data-stu-id="5ee34-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="5ee34-128">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-128">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="5ee34-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="5ee34-130">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-130">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-131">**WM/genre**</span><span class="sxs-lookup"><span data-stu-id="5ee34-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="5ee34-132">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-132">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="5ee34-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="5ee34-134">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-134">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-135">**WM/langage**</span><span class="sxs-lookup"><span data-stu-id="5ee34-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="5ee34-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-137">**Synchronisation des WM et des paroles \_**</span><span class="sxs-lookup"><span data-stu-id="5ee34-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="5ee34-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-139">**WM/humeur**</span><span class="sxs-lookup"><span data-stu-id="5ee34-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="5ee34-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-141">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="5ee34-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="5ee34-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-143">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="5ee34-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="5ee34-144">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-144">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-145">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="5ee34-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="5ee34-146">ASF</span><span class="sxs-lookup"><span data-stu-id="5ee34-146">ASF</span></span>                         |
| [<span data-ttu-id="5ee34-147">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="5ee34-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="5ee34-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="5ee34-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="5ee34-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="5ee34-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="5ee34-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="5ee34-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ee34-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee34-152">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="5ee34-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




