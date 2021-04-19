---
description: Entrelacement de vidéos
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelacement de vidéos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517735"
---
# <a name="video-interlacing"></a><span data-ttu-id="7dd06-103">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="7dd06-103">Video Interlacing</span></span>

<span data-ttu-id="7dd06-104">Cette rubrique décrit comment les sources et les décodeurs multimédias doivent gérer le contenu vidéo entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="7dd06-105">Pour décoder et restituer correctement la vidéo entrelacée, les informations suivantes sont nécessaires :</span><span class="sxs-lookup"><span data-stu-id="7dd06-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="7dd06-106">Progressif ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-106">Progressive or interlaced.</span></span> <span data-ttu-id="7dd06-107">Un flux vidéo peut contenir des images progressives, des images entrelacées ou une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="7dd06-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="7dd06-108">Dominante de champ.</span><span class="sxs-lookup"><span data-stu-id="7dd06-108">Field dominance.</span></span> <span data-ttu-id="7dd06-109">Zone dominante de champ décrit le champ qui apparaît en premier, le champ supérieur ou le champ inférieur.</span><span class="sxs-lookup"><span data-stu-id="7dd06-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="7dd06-110">Répéter le premier champ.</span><span class="sxs-lookup"><span data-stu-id="7dd06-110">Repeat first field.</span></span> <span data-ttu-id="7dd06-111">Cet indicateur est utilisé dans la conversion 3:2, lorsque le frame est progressif mais que le flux est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="7dd06-112">Dans ce contexte, le premier champ peut être le champ supérieur ou inférieur.</span><span class="sxs-lookup"><span data-stu-id="7dd06-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="7dd06-113">Champs entrelacés ou champ unique.</span><span class="sxs-lookup"><span data-stu-id="7dd06-113">Interleaved fields or single field.</span></span> <span data-ttu-id="7dd06-114">Un exemple peut contenir un champ unique ou deux champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="7dd06-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="7dd06-115">Si un échantillon contient un seul champ, la hauteur de l’échantillon correspond à la moitié de la hauteur du cadre, car l’échantillon contient uniquement la moitié des lignes de numérisation d’un cadre.</span><span class="sxs-lookup"><span data-stu-id="7dd06-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="7dd06-116">Les champs entrelacés sont recommandés, à moins que les caractéristiques du contenu source ne stipulent dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="7dd06-117">L’une de ces caractéristiques peut passer d’un exemple à l’autre.</span><span class="sxs-lookup"><span data-stu-id="7dd06-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="7dd06-118">Toutefois, les composants vidéo doivent connaître le contenu global avant le début de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="7dd06-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="7dd06-119">Par exemple, si la vidéo est entrelacée, le convertisseur vidéo amélioré (EVR) doit réserver de la mémoire vidéo pour la désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="7dd06-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="7dd06-120">En revanche, si la vidéo est entièrement progressive, les EVR peuvent optimiser le pipeline de rendu.</span><span class="sxs-lookup"><span data-stu-id="7dd06-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="7dd06-121">L’ajout d’une étape de désentrelacement au pipeline augmente la latence de rendu.</span><span class="sxs-lookup"><span data-stu-id="7dd06-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="7dd06-122">Les informations relatives à l’entrelacement sont stockées à deux emplacements :</span><span class="sxs-lookup"><span data-stu-id="7dd06-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="7dd06-123">Les informations générales sur l’entrelacement dans un flux sont placées dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="7dd06-124">Pour plus d’informations sur les types de médias, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="7dd06-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="7dd06-125">Les informations qui peuvent changer avec chaque exemple sont placées sur l’exemple en tant qu’attribut.</span><span class="sxs-lookup"><span data-stu-id="7dd06-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="7dd06-126">Pour plus d’informations sur les exemples, consultez [Media Samples](media-samples.md)(en anglais).</span><span class="sxs-lookup"><span data-stu-id="7dd06-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="7dd06-127">Entrelacer les informations dans le type de média</span><span class="sxs-lookup"><span data-stu-id="7dd06-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="7dd06-128">L' [**attribut \_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md) sur le type de média décrit comment le flux dans son ensemble est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="7dd06-129">La valeur de cet attribut est un membre de l’énumération [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="7dd06-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="7dd06-130">Un type de média vidéo doit toujours avoir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7dd06-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="7dd06-131">Si le flux contient uniquement des images progressives, sans Frame entrelacé, utilisez MFVideoInterlace \_ progressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="7dd06-132">Si le flux contient uniquement des frames entrelacés et que chaque échantillon contient deux champs entrelacés, utilisez MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="7dd06-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="7dd06-133">Si le flux contient uniquement des frames entrelacés et que chaque exemple contient un champ unique, utilisez MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="7dd06-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="7dd06-134">Si les champs alternent entre le haut et le bas, il n’est pas important d’utiliser ces deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="7dd06-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="7dd06-135">Si le format contient uniquement des champs supérieurs, ou juste des champs inférieurs, définissez la valeur qui correspond au contenu.</span><span class="sxs-lookup"><span data-stu-id="7dd06-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="7dd06-136">Si le flux de contenu contient une combinaison de trames entrelacées et progressives, ou si le champ est défini sur le type de média, définissez le type de support sur MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="7dd06-137">Utilisez des attributs d’exemple pour décrire chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="7dd06-138">Le tableau suivant résume cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7dd06-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="7dd06-139">\_ \_ mode entrelacé MF-MT \_</span><span class="sxs-lookup"><span data-stu-id="7dd06-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="7dd06-140">Entrelacées?</span><span class="sxs-lookup"><span data-stu-id="7dd06-140">Interlaced?</span></span> | <span data-ttu-id="7dd06-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="7dd06-141">Samples</span></span>                                  | <span data-ttu-id="7dd06-142">Premier champ</span><span class="sxs-lookup"><span data-stu-id="7dd06-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="7dd06-143">MFVideoInterlace \_ progressif</span><span class="sxs-lookup"><span data-stu-id="7dd06-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="7dd06-144">Non</span><span class="sxs-lookup"><span data-stu-id="7dd06-144">No</span></span>          | <span data-ttu-id="7dd06-145">Frame progressif</span><span class="sxs-lookup"><span data-stu-id="7dd06-145">Progressive frame</span></span>                        | <span data-ttu-id="7dd06-146">Non applicable</span><span class="sxs-lookup"><span data-stu-id="7dd06-146">Not applicable</span></span> |
| <span data-ttu-id="7dd06-147">MFVideoInterlace \_ FieldInterleavedUpperFirst</span><span class="sxs-lookup"><span data-stu-id="7dd06-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="7dd06-148">Oui</span><span class="sxs-lookup"><span data-stu-id="7dd06-148">Yes</span></span>         | <span data-ttu-id="7dd06-149">Champs entrelacés</span><span class="sxs-lookup"><span data-stu-id="7dd06-149">Interleaved fields</span></span>                       | <span data-ttu-id="7dd06-150">Haut en premier</span><span class="sxs-lookup"><span data-stu-id="7dd06-150">Upper first</span></span>    |
| <span data-ttu-id="7dd06-151">MFVideoInterlace \_ FieldInterleavedLowerFirst</span><span class="sxs-lookup"><span data-stu-id="7dd06-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="7dd06-152">Oui</span><span class="sxs-lookup"><span data-stu-id="7dd06-152">Yes</span></span>         | <span data-ttu-id="7dd06-153">Champs entrelacés</span><span class="sxs-lookup"><span data-stu-id="7dd06-153">Interleaved fields</span></span>                       | <span data-ttu-id="7dd06-154">En premier</span><span class="sxs-lookup"><span data-stu-id="7dd06-154">Lower first</span></span>    |
| <span data-ttu-id="7dd06-155">MFVideoInterlace \_ FieldSingleUpper</span><span class="sxs-lookup"><span data-stu-id="7dd06-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="7dd06-156">Oui</span><span class="sxs-lookup"><span data-stu-id="7dd06-156">Yes</span></span>         | <span data-ttu-id="7dd06-157">Champ unique</span><span class="sxs-lookup"><span data-stu-id="7dd06-157">Single field</span></span>                             | <span data-ttu-id="7dd06-158">Haut en premier</span><span class="sxs-lookup"><span data-stu-id="7dd06-158">Upper first</span></span>    |
| <span data-ttu-id="7dd06-159">MFVideoInterlace \_ FieldSingleLower</span><span class="sxs-lookup"><span data-stu-id="7dd06-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="7dd06-160">Oui</span><span class="sxs-lookup"><span data-stu-id="7dd06-160">Yes</span></span>         | <span data-ttu-id="7dd06-161">Champ unique</span><span class="sxs-lookup"><span data-stu-id="7dd06-161">Single field</span></span>                             | <span data-ttu-id="7dd06-162">En premier</span><span class="sxs-lookup"><span data-stu-id="7dd06-162">Lower first</span></span>    |
| <span data-ttu-id="7dd06-163">MFVideoInterlace \_ MixedInterlaceOrProgressive</span><span class="sxs-lookup"><span data-stu-id="7dd06-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="7dd06-164">Peut varier</span><span class="sxs-lookup"><span data-stu-id="7dd06-164">Can vary</span></span>    | <span data-ttu-id="7dd06-165">Champs entrelacés ou images progressives</span><span class="sxs-lookup"><span data-stu-id="7dd06-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="7dd06-166">Peut varier</span><span class="sxs-lookup"><span data-stu-id="7dd06-166">Can vary</span></span>       |



 

<span data-ttu-id="7dd06-167">Les champs entrelacés et les champs uniques ne peuvent pas être mélangés.</span><span class="sxs-lookup"><span data-stu-id="7dd06-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="7dd06-168">Passer d’un à un autre nécessite une modification de type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="7dd06-169">Entrelacer les indicateurs sur les échantillons</span><span class="sxs-lookup"><span data-stu-id="7dd06-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="7dd06-170">Les informations qui peuvent changer d’un exemple à l’autre sont indiquées à l’aide d’exemples d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7dd06-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="7dd06-171">Utilisez l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour récupérer ou définir ces attributs.</span><span class="sxs-lookup"><span data-stu-id="7dd06-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="7dd06-172">Tous les attributs d’entrelacement listés dans cette section ont des valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="7dd06-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="7dd06-173">En effet, chacun de ces attributs peut avoir trois valeurs : **true**, **false** ou not set.</span><span class="sxs-lookup"><span data-stu-id="7dd06-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="7dd06-174">Si un attribut n’est pas défini, la valeur est extraite du type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="7dd06-175">Si un attribut est défini, la valeur remplace le type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="7dd06-176">Certaines combinaisons d’indicateurs et de types de média ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7dd06-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7dd06-177">Attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-177">Attribute</span></span></th>
<th><span data-ttu-id="7dd06-178">Description</span><span class="sxs-lookup"><span data-stu-id="7dd06-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7dd06-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="7dd06-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="7dd06-180">Si la <strong>valeur est true</strong>, le frame est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="7dd06-181">Si la <strong>valeur est false</strong>, le frame est progressif.</span><span class="sxs-lookup"><span data-stu-id="7dd06-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="7dd06-182">Définissez cet attribut sur chaque exemple si le type de média est MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7dd06-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="7dd06-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="7dd06-184">La signification de cet indicateur varie selon que les exemples contiennent des champs entrelacés ou des champs uniques.</span><span class="sxs-lookup"><span data-stu-id="7dd06-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="7dd06-185">Champs entrelacés : si la <strong>valeur est true</strong>, le champ inférieur est tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="7dd06-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="7dd06-186">Si la <strong>valeur est false</strong>, le champ supérieur est tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="7dd06-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="7dd06-187">Champs uniques : si la <strong>valeur est true</strong>, l’exemple contient un champ inférieur.</span><span class="sxs-lookup"><span data-stu-id="7dd06-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="7dd06-188">Si la <strong>valeur est false</strong>, l’exemple contient un champ supérieur.</span><span class="sxs-lookup"><span data-stu-id="7dd06-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="7dd06-189">Définissez cet attribut sur chaque échantillon entrelacé si le type de média est MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower ou MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7dd06-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="7dd06-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="7dd06-191">Si la <strong>valeur est true</strong>, le premier champ est répété.</span><span class="sxs-lookup"><span data-stu-id="7dd06-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="7dd06-192">Si la valeur est <strong>false</strong> ou non définie, le premier champ n’est pas répété.</span><span class="sxs-lookup"><span data-stu-id="7dd06-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7dd06-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="7dd06-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="7dd06-194">Si la <strong>valeur est true</strong>, l’exemple contient un champ unique.</span><span class="sxs-lookup"><span data-stu-id="7dd06-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="7dd06-195">Si la <strong>valeur est false</strong>, l’exemple contient des champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="7dd06-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7dd06-196">Le tableau suivant indique les indicateurs requis, facultatifs ou interdits, en fonction du type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="7dd06-197">Type de support</span><span class="sxs-lookup"><span data-stu-id="7dd06-197">Media Type</span></span>         | <span data-ttu-id="7dd06-198">Indicateur entrelacé</span><span class="sxs-lookup"><span data-stu-id="7dd06-198">Interlaced Flag</span></span>                      | <span data-ttu-id="7dd06-199">Indicateur BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="7dd06-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="7dd06-200">Indicateur RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="7dd06-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="7dd06-201">Indicateur SingleField</span><span class="sxs-lookup"><span data-stu-id="7dd06-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="7dd06-202">Progressif</span><span class="sxs-lookup"><span data-stu-id="7dd06-202">Progressive</span></span>        | <span data-ttu-id="7dd06-203">Facultatif s’il est défini, doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="7dd06-204">Ne pas définir.</span><span class="sxs-lookup"><span data-stu-id="7dd06-204">Do not set.</span></span>                              | <span data-ttu-id="7dd06-205">Ne pas définir.</span><span class="sxs-lookup"><span data-stu-id="7dd06-205">Do not set.</span></span>           | <span data-ttu-id="7dd06-206">Ne pas définir.</span><span class="sxs-lookup"><span data-stu-id="7dd06-206">Do not set.</span></span>                          |
| <span data-ttu-id="7dd06-207">Champs entrelacés</span><span class="sxs-lookup"><span data-stu-id="7dd06-207">Interleaved fields</span></span> | <span data-ttu-id="7dd06-208">Facultatif Si cette propriété est définie, elle doit avoir la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="7dd06-209">Facultatif Si cette valeur est définie, doit correspondre au type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="7dd06-210">Ne pas définir.</span><span class="sxs-lookup"><span data-stu-id="7dd06-210">Do not set.</span></span>           | <span data-ttu-id="7dd06-211">Facultatif s’il est défini, doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="7dd06-212">Champs uniques</span><span class="sxs-lookup"><span data-stu-id="7dd06-212">Single fields</span></span>      | <span data-ttu-id="7dd06-213">Facultatif Si cette propriété est définie, elle doit avoir la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="7dd06-214">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-214">Required.</span></span>                                | <span data-ttu-id="7dd06-215">Ne pas définir.</span><span class="sxs-lookup"><span data-stu-id="7dd06-215">Do not set.</span></span>           | <span data-ttu-id="7dd06-216">Affectez la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="7dd06-217">Mixte</span><span class="sxs-lookup"><span data-stu-id="7dd06-217">Mixed</span></span>              | <span data-ttu-id="7dd06-218">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-218">Required.</span></span>                            | <span data-ttu-id="7dd06-219">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-219">Required.</span></span>                                | <span data-ttu-id="7dd06-220">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-220">Required.</span></span>             | <span data-ttu-id="7dd06-221">Facultatif s’il est défini, doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="7dd06-222">Dans les cas où l’attribut est facultatif, le type de média définit déjà les informations.</span><span class="sxs-lookup"><span data-stu-id="7dd06-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="7dd06-223">Il est possible de définir l’attribut pour qu’il corresponde, mais ce n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7dd06-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="7dd06-224">Par exemple, si le type de média est \_ progressif MFVideoInterlace, cela implique que toutes les trames dans le flux sont progressives.</span><span class="sxs-lookup"><span data-stu-id="7dd06-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="7dd06-225">Par conséquent, vous pouvez définir l' **attribut \_ entrelacé MFSampleExtension** sur **false** ou conserver l’attribut unset.</span><span class="sxs-lookup"><span data-stu-id="7dd06-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="7dd06-226">Recommandations</span><span class="sxs-lookup"><span data-stu-id="7dd06-226">Recommendations</span></span>

<span data-ttu-id="7dd06-227">Cette section contient des recommandations pour différents types de contenu.</span><span class="sxs-lookup"><span data-stu-id="7dd06-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="7dd06-228">La vidéo est l’ensemble des trames progressives.</span><span class="sxs-lookup"><span data-stu-id="7dd06-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="7dd06-229">Définissez le type de média sur MFVideoInterlace \_ progressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="7dd06-230">Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **false** sur chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="7dd06-231">Ne définissez pas les attributs **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** ou **MFSampleExtension \_ SingleField** .</span><span class="sxs-lookup"><span data-stu-id="7dd06-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="7dd06-232">La vidéo est l’ensemble des champs entrelacés avec la même dominante de champ.</span><span class="sxs-lookup"><span data-stu-id="7dd06-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="7dd06-233">Les exemples contiennent des champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="7dd06-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="7dd06-234">Définissez le type de média sur MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="7dd06-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="7dd06-235">Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **true** sur chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="7dd06-236">Ne définissez pas l’attribut **MFSampleExtension \_ BottomFieldFirst** , ou définissez la valeur de chaque frame pour qu’elle corresponde au type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="7dd06-237">Ne définissez pas l’attribut **MFSampleExtension \_ RepeatFirstField** , ou affectez-lui la valeur **false** pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="7dd06-238">Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **false** pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="7dd06-239">La vidéo contient une combinaison d’images entrelacées et progressives, avec des champs répétés et une dominante de champ variable (par exemple, DVD vidéo).</span><span class="sxs-lookup"><span data-stu-id="7dd06-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="7dd06-240">Définissez le type de média sur MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="7dd06-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="7dd06-241">Sur chaque trame, définissez les attributs **MFSampleExtension \_ entrelacé**, **MFSampleExtension \_ BottomFieldFirst** et **MFSampleExtension \_ RepeatFirstField** .</span><span class="sxs-lookup"><span data-stu-id="7dd06-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="7dd06-242">Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **false** pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="7dd06-243">La vidéo est entrelacée et les exemples contiennent des champs uniques.</span><span class="sxs-lookup"><span data-stu-id="7dd06-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="7dd06-244">Définissez le type de média sur MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="7dd06-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="7dd06-245">Sur chaque trame, définissez l’attribut **MFSampleExtension \_ BottomFieldFirst** .</span><span class="sxs-lookup"><span data-stu-id="7dd06-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="7dd06-246">Ne définissez pas l' **attribut \_ entrelacé MFSampleExtension** ou affectez-lui la valeur **true** sur chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="7dd06-247">Ne définissez pas l’attribut **MFSampleExtension \_ RepeatFirstField** , ou affectez-lui la valeur **false** pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="7dd06-248">Ne définissez pas l’attribut **MFSampleExtension \_ SingleField** , ou affectez-lui la valeur **true** sur chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7dd06-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="7dd06-249">La plupart des contenus vidéo appartiennent à l’une de ces catégories.</span><span class="sxs-lookup"><span data-stu-id="7dd06-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="7dd06-250">Mappages MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7dd06-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="7dd06-251">Pour le contenu MPEG-2, utilisez les mappages suivants pour convertir les indicateurs MPEG-2 en Media Foundation exemples d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7dd06-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="7dd06-252">**structure d’image \_**</span><span class="sxs-lookup"><span data-stu-id="7dd06-252">**picture\_structure**</span></span>



| <span data-ttu-id="7dd06-253">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd06-253">Value</span></span>         | <span data-ttu-id="7dd06-254">Exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd06-255">frame</span><span class="sxs-lookup"><span data-stu-id="7dd06-255">frame</span></span>         | <span data-ttu-id="7dd06-256">**MFSampleExtension \_ SingleField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="7dd06-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="7dd06-257">champ du haut \_</span><span class="sxs-lookup"><span data-stu-id="7dd06-257">top\_field</span></span>    | <span data-ttu-id="7dd06-258">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="7dd06-259">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="7dd06-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="7dd06-260">champ du bas \_</span><span class="sxs-lookup"><span data-stu-id="7dd06-260">bottom\_field</span></span> | <span data-ttu-id="7dd06-261">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="7dd06-262">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="7dd06-263">**Frame progressif \_**</span><span class="sxs-lookup"><span data-stu-id="7dd06-263">**progressive\_frame**</span></span>



| <span data-ttu-id="7dd06-264">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd06-264">Value</span></span> | <span data-ttu-id="7dd06-265">Exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="7dd06-266">0</span><span class="sxs-lookup"><span data-stu-id="7dd06-266">0</span></span>     | <span data-ttu-id="7dd06-267">**MFSampleExtension \_ Entrelacé**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="7dd06-268">1</span><span class="sxs-lookup"><span data-stu-id="7dd06-268">1</span></span>     | <span data-ttu-id="7dd06-269">**MFSampleExtension \_**  =  **False** entrelacé</span><span class="sxs-lookup"><span data-stu-id="7dd06-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="7dd06-270">**champ supérieur en \_ \_ premier**</span><span class="sxs-lookup"><span data-stu-id="7dd06-270">**top\_field\_first**</span></span>



| <span data-ttu-id="7dd06-271">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd06-271">Value</span></span> | <span data-ttu-id="7dd06-272">Exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="7dd06-273">0</span><span class="sxs-lookup"><span data-stu-id="7dd06-273">0</span></span>     | <span data-ttu-id="7dd06-274">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="7dd06-275">1</span><span class="sxs-lookup"><span data-stu-id="7dd06-275">1</span></span>     | <span data-ttu-id="7dd06-276">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="7dd06-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="7dd06-277">**répéter le \_ premier \_ champ**</span><span class="sxs-lookup"><span data-stu-id="7dd06-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="7dd06-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dd06-278">Value</span></span> | <span data-ttu-id="7dd06-279">Exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="7dd06-280">0</span><span class="sxs-lookup"><span data-stu-id="7dd06-280">0</span></span>     | <span data-ttu-id="7dd06-281">**MFSampleExtension \_ RepeatFirstField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="7dd06-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="7dd06-282">1</span><span class="sxs-lookup"><span data-stu-id="7dd06-282">1</span></span>     | <span data-ttu-id="7dd06-283">**MFSampleExtension \_ RepeatFirstField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="7dd06-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="7dd06-284">Exemples de Single-Field</span><span class="sxs-lookup"><span data-stu-id="7dd06-284">Single-Field Samples</span></span>

<span data-ttu-id="7dd06-285">Si le type de média est MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower, cela signifie que chaque échantillon contient un champ unique.</span><span class="sxs-lookup"><span data-stu-id="7dd06-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="7dd06-286">Toutefois, le type de média décrit le frame entier.</span><span class="sxs-lookup"><span data-stu-id="7dd06-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="7dd06-287">Par conséquent, chaque mémoire tampon contient uniquement la moitié du nombre de lignes de champs fournies dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="7dd06-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="7dd06-288">Par exemple, si le type de média décrit la vidéo sous la forme 720 × 480, chaque champ contient 240 lignes de numérisation, et par conséquent, chaque mémoire tampon contient uniquement 240 lignes de pixels.</span><span class="sxs-lookup"><span data-stu-id="7dd06-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="7dd06-289">Si vous écrivez un composant qui accepte des types de média avec des exemples à champ unique, vous devez prendre ce fait en compte lorsque vous accédez aux données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7dd06-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="7dd06-290">La même règle s’applique à l’ouverture géométrique (attribut d'[ \_ \_ \_ ouverture géométrique MF MT](mf-mt-geometric-aperture-attribute.md) ) et à l’ouverture de l’affichage minimale (attribut d’ouverture d’affichage de l'[ \_ affichage MF MT \_ minimum \_ \_ ](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="7dd06-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="7dd06-291">Ces régions sont spécifiées en termes d’ensemble du cadre, et non des champs individuels.</span><span class="sxs-lookup"><span data-stu-id="7dd06-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="7dd06-292">Mappages DirectShow</span><span class="sxs-lookup"><span data-stu-id="7dd06-292">DirectShow Mappings</span></span>

<span data-ttu-id="7dd06-293">Dans DirectShow, les informations d’entrelacement par échantillon sont contenues dans le membre **dwTypeSpecificFlags** de la structure de **\_ \_ Propriétés am SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="7dd06-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="7dd06-294">Le tableau suivant présente les attributs équivalents pour Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7dd06-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="7dd06-295">Exemple d’indicateur DirectShow</span><span class="sxs-lookup"><span data-stu-id="7dd06-295">DirectShow sample flag</span></span>              | <span data-ttu-id="7dd06-296">Media Foundation l’exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd06-297">image de l' \_ \_ indicateur vidéo \_ entrelacé \_</span><span class="sxs-lookup"><span data-stu-id="7dd06-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="7dd06-298">**MFSampleExtension \_ SingleField**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="7dd06-299">\_Indicateur de vidéo am \_ \_ champ1</span><span class="sxs-lookup"><span data-stu-id="7dd06-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="7dd06-300">**MFSampleExtension \_**  =  **True** entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="7dd06-301">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="7dd06-302">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="7dd06-303">\_Indicateur vidéo \_ am \_ champ2</span><span class="sxs-lookup"><span data-stu-id="7dd06-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="7dd06-304">**MFSampleExtension \_**  =  **True** entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="7dd06-305">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="7dd06-306">**MFSampleExtension \_ BottomFieldFirst**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="7dd06-307">\_indicateur vidéo \_ am \_ tissage</span><span class="sxs-lookup"><span data-stu-id="7dd06-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="7dd06-308">**MFSampleExtension \_**  =  **False** entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="7dd06-309">(Cet indicateur indique que le pilote ne doit pas désentrelacer les deux champs.)</span><span class="sxs-lookup"><span data-stu-id="7dd06-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="7dd06-310">\_Indicateur vidéo \_ am \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="7dd06-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="7dd06-311">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="7dd06-312">Si le contenu est entrelacé et que l’indicateur AM \_ Video \_ Flag \_ FIELD1FIRST n’est pas présent, affectez la valeur **true** à cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7dd06-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="7dd06-313">champ de répétition de l' \_ indicateur vidéo am \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7dd06-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="7dd06-314">**MFSampleExtension \_ RepeatFirstField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="7dd06-315">Si l' \_ indicateur de champ REPEAT de l’indicateur de vidéo am \_ \_ \_ n’est pas présent, affectez la valeur **false** à cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7dd06-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="7dd06-316">Si l’exemple DirectShow ne contient pas d’indicateurs d’échantillon, utilisez la valeur de **dwInterlaceFlags** à partir de la structure **VIDEOINFOHEADER2** :</span><span class="sxs-lookup"><span data-stu-id="7dd06-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="7dd06-317">Indicateur entrelacé DirectShow</span><span class="sxs-lookup"><span data-stu-id="7dd06-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="7dd06-318">Media Foundation l’exemple d’attribut</span><span class="sxs-lookup"><span data-stu-id="7dd06-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="7dd06-319">AMINTERLACE \_ IsInterlaced</span><span class="sxs-lookup"><span data-stu-id="7dd06-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="7dd06-320">**MFSampleExtension \_**  =  **True** entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7dd06-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="7dd06-321">AMINTERLACE \_ 1FieldPerSample</span><span class="sxs-lookup"><span data-stu-id="7dd06-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="7dd06-322">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="7dd06-323">AMINTERLACE \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="7dd06-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="7dd06-324">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="7dd06-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7dd06-325">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7dd06-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dd06-326">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="7dd06-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="7dd06-327">Types de médias</span><span class="sxs-lookup"><span data-stu-id="7dd06-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




