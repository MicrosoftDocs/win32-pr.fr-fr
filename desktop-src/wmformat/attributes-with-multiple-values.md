---
title: Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media format 11)
description: Attributs avec plusieurs valeurs
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, valeurs multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032204"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="28067-107">Attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="28067-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="28067-108">Plusieurs valeurs peuvent être assignées à certains des attributs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="28067-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="28067-109">Par exemple, **Artist** est un attribut qui peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="28067-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="28067-110">Vous pouvez appeler [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) plusieurs fois pour ajouter autant de valeurs d' **artistes** que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="28067-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="28067-111">Si vous effectuez plusieurs appels à **AddAttribute** pour les attributs qui ne prennent pas en charge plusieurs valeurs, la méthode peut retourner un code d’erreur ou ignorer simplement votre demande.</span><span class="sxs-lookup"><span data-stu-id="28067-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="28067-112">Le tableau suivant répertorie les attributs qui prennent en charge plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="28067-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="28067-113">Certains attributs peuvent avoir plusieurs valeurs uniquement dans des fichiers ASF, tandis que d’autres peuvent avoir plusieurs valeurs dans des fichiers ASF et MP3.</span><span class="sxs-lookup"><span data-stu-id="28067-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="28067-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="28067-114">Attribute</span></span>                                                 | <span data-ttu-id="28067-115">Prise en charge de plusieurs valeurs</span><span class="sxs-lookup"><span data-stu-id="28067-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="28067-116">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="28067-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="28067-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-118">**WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="28067-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="28067-119">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-119">ASF</span></span>                         |
| [<span data-ttu-id="28067-120">**WM/AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="28067-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="28067-121">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-121">ASF</span></span>                         |
| [<span data-ttu-id="28067-122">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="28067-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="28067-123">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-123">ASF</span></span>                         |
| [<span data-ttu-id="28067-124">**WM/composer**</span><span class="sxs-lookup"><span data-stu-id="28067-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="28067-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-126">**WM/conducteur**</span><span class="sxs-lookup"><span data-stu-id="28067-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="28067-127">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-127">ASF</span></span>                         |
| [<span data-ttu-id="28067-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="28067-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="28067-129">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-129">ASF</span></span>                         |
| [<span data-ttu-id="28067-130">**WM/genre**</span><span class="sxs-lookup"><span data-stu-id="28067-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="28067-131">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-131">ASF</span></span>                         |
| [<span data-ttu-id="28067-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="28067-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="28067-133">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-133">ASF</span></span>                         |
| [<span data-ttu-id="28067-134">**WM/langage**</span><span class="sxs-lookup"><span data-stu-id="28067-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="28067-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-136">**Synchronisation des WM et des paroles \_**</span><span class="sxs-lookup"><span data-stu-id="28067-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="28067-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-138">**WM/humeur**</span><span class="sxs-lookup"><span data-stu-id="28067-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="28067-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-140">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="28067-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="28067-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-142">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="28067-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="28067-143">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-143">ASF</span></span>                         |
| [<span data-ttu-id="28067-144">**WM/PromotionURL**</span><span class="sxs-lookup"><span data-stu-id="28067-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="28067-145">ASF</span><span class="sxs-lookup"><span data-stu-id="28067-145">ASF</span></span>                         |
| [<span data-ttu-id="28067-146">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="28067-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="28067-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="28067-148">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="28067-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="28067-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="28067-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="28067-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28067-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28067-151">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="28067-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




