---
title: Élément ASX
description: L’élément ASX définit un fichier en tant que métafichier.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Élément ASX lecteur Windows Media
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521679"
---
# <a name="asx-element"></a><span data-ttu-id="7090d-104">Élément ASX</span><span class="sxs-lookup"><span data-stu-id="7090d-104">ASX Element</span></span>

<span data-ttu-id="7090d-105">L’élément **ASX** définit un fichier en tant que métafichier.</span><span class="sxs-lookup"><span data-stu-id="7090d-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="7090d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="7090d-106">Attributes</span></span>

<span data-ttu-id="7090d-107">`VERSION` (requis)</span><span class="sxs-lookup"><span data-stu-id="7090d-107">`VERSION` (required)</span></span>

<span data-ttu-id="7090d-108">Nombre décimal représentant le numéro de version de la syntaxe pour le métafichier.</span><span class="sxs-lookup"><span data-stu-id="7090d-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="7090d-109">Défini sur 3 ou 3,0.</span><span class="sxs-lookup"><span data-stu-id="7090d-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="7090d-110">**PREVIEWMODE** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7090d-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="7090d-111">Valeur indiquant si le lecteur Windows Media passe en mode aperçu avant de lancer le premier clip.</span><span class="sxs-lookup"><span data-stu-id="7090d-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="7090d-112">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7090d-112">Must be one of the following values.</span></span>



| <span data-ttu-id="7090d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7090d-113">Value</span></span> | <span data-ttu-id="7090d-114">Description</span><span class="sxs-lookup"><span data-stu-id="7090d-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7090d-115">YES</span><span class="sxs-lookup"><span data-stu-id="7090d-115">YES</span></span>   | <span data-ttu-id="7090d-116">Le lecteur Windows Media passe en mode aperçu avant de visionner le premier clip.</span><span class="sxs-lookup"><span data-stu-id="7090d-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="7090d-117">Non</span><span class="sxs-lookup"><span data-stu-id="7090d-117">NO</span></span>    | <span data-ttu-id="7090d-118">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7090d-118">The default value.</span></span> <span data-ttu-id="7090d-119">Le lecteur Windows Media n’entre pas en mode aperçu avant de commencer le premier clip.</span><span class="sxs-lookup"><span data-stu-id="7090d-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="7090d-120">**BANNERBAR** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7090d-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="7090d-121">Valeur indiquant si le lecteur Windows Media réserve de l’espace pour un graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="7090d-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="7090d-122">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7090d-122">Must be one of the following values.</span></span>



| <span data-ttu-id="7090d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7090d-123">Value</span></span> | <span data-ttu-id="7090d-124">Description</span><span class="sxs-lookup"><span data-stu-id="7090d-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7090d-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="7090d-125">AUTO</span></span>  | <span data-ttu-id="7090d-126">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7090d-126">The default value.</span></span> <span data-ttu-id="7090d-127">Le lecteur Windows Media réserve de l’espace pour la barre de bannière uniquement lorsqu’un élément de contenu en contient un.</span><span class="sxs-lookup"><span data-stu-id="7090d-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="7090d-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="7090d-128">FIXED</span></span> | <span data-ttu-id="7090d-129">Le lecteur Windows Media réserve un espace fixe pour un graphique de bannière pour chaque morceau de contenu lu, qu’il y ait une bannière associée.</span><span class="sxs-lookup"><span data-stu-id="7090d-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="7090d-130">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="7090d-130">Parent/Child Elements</span></span>



| <span data-ttu-id="7090d-131">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="7090d-131">Hierarchy</span></span>       | <span data-ttu-id="7090d-132">Éléments</span><span class="sxs-lookup"><span data-stu-id="7090d-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7090d-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7090d-133">Parent elements</span></span> | <span data-ttu-id="7090d-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="7090d-134">None.</span></span> <span data-ttu-id="7090d-135">L’élément **ASX** doit être le premier élément de chaque métafichier.</span><span class="sxs-lookup"><span data-stu-id="7090d-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="7090d-136">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7090d-136">Child elements</span></span>  | <span data-ttu-id="7090d-137">**abstract**, **Author**, **Banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **moreinfo**, **PREVIEWDURATION**, **param**, **REPEAT**, **title**</span><span class="sxs-lookup"><span data-stu-id="7090d-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7090d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="7090d-138">Remarks</span></span>

<span data-ttu-id="7090d-139">Les quatre premiers caractères d’une sélection de métafichiers doivent être « <ASX ».</span><span class="sxs-lookup"><span data-stu-id="7090d-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="7090d-140">Les autres éléments définis dans l’étendue de l’élément **ASX** , tels que **title** et **Author**, sont associés aux informations affichées par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7090d-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="7090d-141">Pour le lecteur Windows Media, le numéro de version de la syntaxe est 3,0.</span><span class="sxs-lookup"><span data-stu-id="7090d-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="7090d-142">Le lecteur Windows Media prend en charge toutes les versions précédentes de la syntaxe Metafile.</span><span class="sxs-lookup"><span data-stu-id="7090d-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="7090d-143">Les valeurs acceptables pour l’attribut **version** incluent à la fois 3,0 et 3 (sans virgule décimale).</span><span class="sxs-lookup"><span data-stu-id="7090d-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="7090d-144">Si la valeur de l’attribut **PREVIEWMODE** est Yes, le lecteur Windows Media passe immédiatement en mode aperçu avant de lancer le premier clip.</span><span class="sxs-lookup"><span data-stu-id="7090d-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="7090d-145">Lorsque le lecteur Windows Media passe en mode aperçu, il affiche un aperçu de chaque clip référencé dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="7090d-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="7090d-146">L’élément **PREVIEWDURATION** détermine la durée de chaque aperçu.</span><span class="sxs-lookup"><span data-stu-id="7090d-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="7090d-147">L’attribut **BANNERBAR** définit si le lecteur Windows Media réserve de l’espace pour un graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="7090d-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="7090d-148">Une bannière est un graphique qui s’affiche dans la zone d’affichage vidéo pendant la diffusion du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="7090d-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="7090d-149">(Utilisez l’élément **bannière** pour ajouter une bannière au contenu.) Si la valeur de **BANNERBAR** est fixe, le lecteur Windows Media réserve de l’espace de bannière pour chaque contenu multimédia, que le contenu du média ait une bannière.</span><span class="sxs-lookup"><span data-stu-id="7090d-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="7090d-150">Si un contenu multimédia n’est associé à aucune bannière, l’espace réservé pour celui-ci est noir.</span><span class="sxs-lookup"><span data-stu-id="7090d-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="7090d-151">Si la valeur de l’attribut **BANNERBAR** est auto, le lecteur Windows Media réserve de l’espace pour la bannière uniquement lorsque le contenu multimédia en contient un.</span><span class="sxs-lookup"><span data-stu-id="7090d-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="7090d-152">Si vous créez un métafichier avec plusieurs clips (éléments **entry** ou **ENTRYREF** ) et que vous définissez la valeur de l’attribut **BANNERBAR** sur auto, le lecteur Windows Media peut se redimensionner pour permettre l’espace pour un graphique de bannière pour un clip, puis le redimensionner si le clip suivant ne contient pas de graphique de bannière.</span><span class="sxs-lookup"><span data-stu-id="7090d-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="7090d-153">Si vous souhaitez que la taille de la fenêtre reste la même (sauf en cas de modification de la taille de la vidéo), utilisez la valeur fixe de l’attribut **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="7090d-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="7090d-154">L’espace réservé pour un graphique de bannière est de 32 pixels de haut en 194 pixels de large.</span><span class="sxs-lookup"><span data-stu-id="7090d-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="7090d-155">L’espace réservé apparaît en dessous du contenu vidéo rendu et de 6 pixels au-dessus du bord inférieur de la zone vidéo, ce qui permet d’obtenir de l’espace pour la bordure de la zone vidéo de 6 pixels.</span><span class="sxs-lookup"><span data-stu-id="7090d-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="7090d-156">L’espace de bannière réservé est centré horizontalement.</span><span class="sxs-lookup"><span data-stu-id="7090d-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="7090d-157">Le lecteur Windows Media effectue le rendu du graphique à partir du pixel le plus à gauche de l’espace de la bannière.</span><span class="sxs-lookup"><span data-stu-id="7090d-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="7090d-158">Si le graphique remplit la totalité de l’espace, il s’affiche centré horizontalement.</span><span class="sxs-lookup"><span data-stu-id="7090d-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="7090d-159">Dans le cas contraire, il y aura un espace de fin.</span><span class="sxs-lookup"><span data-stu-id="7090d-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="7090d-160">Notez que la largeur minimale du lecteur Windows Media est toujours plus large que la taille du clip vidéo, quelle que soit la valeur de l’attribut **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="7090d-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="7090d-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="7090d-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="7090d-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7090d-162">Requirements</span></span>



| <span data-ttu-id="7090d-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7090d-163">Requirement</span></span> | <span data-ttu-id="7090d-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="7090d-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="7090d-165">Version</span><span class="sxs-lookup"><span data-stu-id="7090d-165">Version</span></span><br/> | <span data-ttu-id="7090d-166">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7090d-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7090d-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7090d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7090d-168">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7090d-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7090d-169">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7090d-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





