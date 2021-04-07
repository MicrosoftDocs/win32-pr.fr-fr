---
title: Ordre de priorité
description: Ordre de priorité
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Sous-fichiers Windows Media, ordre de priorité
- Fichiers Windows Media, priorité
- sous-fichiers, ordre de priorité
- fichiers de préversion, précédence
- Windows Media, sous-fichiers
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028863"
---
# <a name="order-of-precedence"></a><span data-ttu-id="afe0e-108">Ordre de priorité</span><span class="sxs-lookup"><span data-stu-id="afe0e-108">Order of Precedence</span></span>

<span data-ttu-id="afe0e-109">Tous les attributs d’élément de métafichier ne sont pas égaux.</span><span class="sxs-lookup"><span data-stu-id="afe0e-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="afe0e-110">Certains attributs d’éléments de métafichier remplacent d’autres attributs d’élément.</span><span class="sxs-lookup"><span data-stu-id="afe0e-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="afe0e-111">Les attributs d’élément peuvent être remplacés par des attributs d’élément similaires en fonction de la position et de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="afe0e-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="afe0e-112">Tous les attributs d’une sélection de métafichier remplacent ceux contenus dans un fichier Windows Media référencé.</span><span class="sxs-lookup"><span data-stu-id="afe0e-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="afe0e-113">Un attribut qui remplace un autre a une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="afe0e-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="afe0e-114">La hiérarchie, prioritaire vers la plus faible, est indiquée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="afe0e-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="afe0e-115">L’élément de priorité la plus élevée n’est jamais remplacé.</span><span class="sxs-lookup"><span data-stu-id="afe0e-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="afe0e-116">Étendue</span><span class="sxs-lookup"><span data-stu-id="afe0e-116">Scope</span></span>                    | <span data-ttu-id="afe0e-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="afe0e-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="afe0e-118">« Contenu DRM signé »</span><span class="sxs-lookup"><span data-stu-id="afe0e-118">"Signed DRM content"</span></span>     | <span data-ttu-id="afe0e-119">Jamais substitué.</span><span class="sxs-lookup"><span data-stu-id="afe0e-119">Never overridden.</span></span>                           |
| <span data-ttu-id="afe0e-120">Portée de l’élément de **référence**</span><span class="sxs-lookup"><span data-stu-id="afe0e-120">**REF** element scope</span></span>    | <span data-ttu-id="afe0e-121">Substitué uniquement par du contenu DRM signé.</span><span class="sxs-lookup"><span data-stu-id="afe0e-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="afe0e-122">Portée de l’élément d' **entrée**</span><span class="sxs-lookup"><span data-stu-id="afe0e-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="afe0e-123">Remplace les éléments des catégories ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="afe0e-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="afe0e-124">Étendue **ASX**</span><span class="sxs-lookup"><span data-stu-id="afe0e-124">**ASX** scope</span></span>            | <span data-ttu-id="afe0e-125">Remplace les éléments du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="afe0e-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="afe0e-126">Étendue du fichier Windows Media</span><span class="sxs-lookup"><span data-stu-id="afe0e-126">Windows Media file scope</span></span> | <span data-ttu-id="afe0e-127">Remplacé par tous les éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="afe0e-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="afe0e-128">« Contenu DRM signé »-objet de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="afe0e-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="afe0e-129">Les attributs du contenu DRM signé remplacent tous les autres.</span><span class="sxs-lookup"><span data-stu-id="afe0e-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="afe0e-130">Par exemple, les informations de copyright de « contenu DRM signé » ne seront pas remplacées.</span><span class="sxs-lookup"><span data-stu-id="afe0e-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="afe0e-131">Elle sera toujours diffusée en continu et présentée.</span><span class="sxs-lookup"><span data-stu-id="afe0e-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="afe0e-132">Portée de l’élément de **référence**</span><span class="sxs-lookup"><span data-stu-id="afe0e-132">**REF** element scope</span></span>

    <span data-ttu-id="afe0e-133">Les attributs de l’élément **ref** remplacent les autres attributs d’élément, mais pas le contenu DRM signé.</span><span class="sxs-lookup"><span data-stu-id="afe0e-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="afe0e-134">Étendue de l' **entrée**</span><span class="sxs-lookup"><span data-stu-id="afe0e-134">**ENTRY** scope</span></span>

    <span data-ttu-id="afe0e-135">Les attributs de l’élément **entry** seront remplacés par l’attribut de l’élément **ref** , mais ils remplaceront les autres attributs d’élément.</span><span class="sxs-lookup"><span data-stu-id="afe0e-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="afe0e-136">Les métadonnées de **titre** de l’élément **entry** s’affichent à la place des informations de titre du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="afe0e-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="afe0e-137">Étendue **ASX**</span><span class="sxs-lookup"><span data-stu-id="afe0e-137">**ASX** scope</span></span>

    <span data-ttu-id="afe0e-138">Toutes les propriétés entrées dans le métafichier remplacent celles contenues dans le fichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afe0e-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="afe0e-139">Les attributs de l’élément **entry** remplacent les attributs de l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="afe0e-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="afe0e-140">Pendant la diffusion du clip multimédia référencé de l’élément d' **entrée** , les métadonnées de **titre** de l’élément d' **entrée** sont affichées à la place des informations de titre de l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="afe0e-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="afe0e-141">Étendue du fichier Windows Media</span><span class="sxs-lookup"><span data-stu-id="afe0e-141">Windows Media file scope</span></span>

    <span data-ttu-id="afe0e-142">Les attributs du fichier Windows Media sont remplacés par n’importe quel attribut de métafichier.</span><span class="sxs-lookup"><span data-stu-id="afe0e-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="afe0e-143">Les métadonnées de fichier multimédia s’affichent uniquement si aucune métadonnée n’est définie pour cet élément dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="afe0e-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afe0e-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afe0e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe0e-145">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="afe0e-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="afe0e-146">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="afe0e-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="afe0e-147">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="afe0e-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="afe0e-148">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="afe0e-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




