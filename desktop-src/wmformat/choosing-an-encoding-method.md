---
title: Choix d’une méthode d’encodage
description: Choix d’une méthode d’encodage
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- profils, choix des méthodes d’encodage
- profils, méthodes d’encodage
- codecs, choix des méthodes d’encodage
- codecs, méthodes d’encodage
- profils, sélection des méthodes d’encodage
- codecs, sélection des méthodes d’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511822"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="421ca-109">Choix d’une méthode d’encodage</span><span class="sxs-lookup"><span data-stu-id="421ca-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="421ca-110">Certains codecs, comme le codec Windows Media Video 9, prennent en charge plusieurs méthodes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="421ca-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="421ca-111">La méthode d’encodage que vous choisissez pour un flux dépend de la façon dont le flux doit être remis.</span><span class="sxs-lookup"><span data-stu-id="421ca-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="421ca-112">Le tableau suivant décrit quand utiliser les différentes méthodes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="421ca-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="421ca-113">Méthode de codage</span><span class="sxs-lookup"><span data-stu-id="421ca-113">Encoding method</span></span>                | <span data-ttu-id="421ca-114">Description</span><span class="sxs-lookup"><span data-stu-id="421ca-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="421ca-115">Vitesse de transmission constante en 1 passe (CBR)</span><span class="sxs-lookup"><span data-stu-id="421ca-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="421ca-116">La seule option pour la diffusion en continu en direct.</span><span class="sxs-lookup"><span data-stu-id="421ca-116">The only option for live streaming.</span></span> <span data-ttu-id="421ca-117">Encode une vitesse de transmission prévisible et fournit la qualité la plus faible de toutes les méthodes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="421ca-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="421ca-118">2-pass CBR</span><span class="sxs-lookup"><span data-stu-id="421ca-118">2-pass CBR</span></span>                     | <span data-ttu-id="421ca-119">Utilisez pour les fichiers qui seront diffusés en continu sur un réseau vers un lecteur client, mais qui ne sont pas diffusés à partir d’une source active.</span><span class="sxs-lookup"><span data-stu-id="421ca-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="421ca-120">Encode une vitesse de transmission prévisible, mais avec une qualité supérieure à 1-pass CBR.</span><span class="sxs-lookup"><span data-stu-id="421ca-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="421ca-121">Vitesse de transmission variable (VBR) de passe 1</span><span class="sxs-lookup"><span data-stu-id="421ca-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="421ca-122">Utilisez lorsque vous devez spécifier la qualité de la sortie encodée.</span><span class="sxs-lookup"><span data-stu-id="421ca-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="421ca-123">Offre la qualité la plus cohérente de toutes les méthodes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="421ca-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="421ca-124">À utiliser uniquement pour les fichiers locaux ou pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="421ca-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="421ca-125">2-pass VBR – sans contrainte</span><span class="sxs-lookup"><span data-stu-id="421ca-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="421ca-126">Utilisez lorsque vous devez spécifier une bande passante, mais que des fluctuations autour de la bande passante spécifiée sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="421ca-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="421ca-127">Pour les fichiers locaux ou uniquement pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="421ca-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="421ca-128">2-passer le VBR-restreint</span><span class="sxs-lookup"><span data-stu-id="421ca-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="421ca-129">Utilisez dans les mêmes conditions que sans contrainte, mais lorsque vous devez spécifier un taux de bits momentané maximal.</span><span class="sxs-lookup"><span data-stu-id="421ca-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="421ca-130">Pour les fichiers locaux ou uniquement pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="421ca-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="421ca-131">Le tableau suivant répertorie les méthodes d’encodage prises en charge par les codecs fournis avec le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="421ca-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="421ca-132">Codec</span><span class="sxs-lookup"><span data-stu-id="421ca-132">Codec</span></span>                                  | <span data-ttu-id="421ca-133">CBR</span><span class="sxs-lookup"><span data-stu-id="421ca-133">CBR</span></span> | <span data-ttu-id="421ca-134">2-pass CBR</span><span class="sxs-lookup"><span data-stu-id="421ca-134">2-pass CBR</span></span> | <span data-ttu-id="421ca-135">MODE VBR</span><span class="sxs-lookup"><span data-stu-id="421ca-135">VBR</span></span> | <span data-ttu-id="421ca-136">2-passer le VBR</span><span class="sxs-lookup"><span data-stu-id="421ca-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="421ca-137">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="421ca-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="421ca-138">X</span><span class="sxs-lookup"><span data-stu-id="421ca-138">X</span></span>   | <span data-ttu-id="421ca-139">X</span><span class="sxs-lookup"><span data-stu-id="421ca-139">X</span></span>          | <span data-ttu-id="421ca-140">X</span><span class="sxs-lookup"><span data-stu-id="421ca-140">X</span></span>   | <span data-ttu-id="421ca-141">X</span><span class="sxs-lookup"><span data-stu-id="421ca-141">X</span></span>          |
| <span data-ttu-id="421ca-142">Windows Media Audio 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="421ca-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="421ca-143">X</span><span class="sxs-lookup"><span data-stu-id="421ca-143">X</span></span>   | <span data-ttu-id="421ca-144">X</span><span class="sxs-lookup"><span data-stu-id="421ca-144">X</span></span>          | <span data-ttu-id="421ca-145">X</span><span class="sxs-lookup"><span data-stu-id="421ca-145">X</span></span>   | <span data-ttu-id="421ca-146">X</span><span class="sxs-lookup"><span data-stu-id="421ca-146">X</span></span>          |
| <span data-ttu-id="421ca-147">Écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="421ca-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="421ca-148">X</span><span class="sxs-lookup"><span data-stu-id="421ca-148">X</span></span>   |            | <span data-ttu-id="421ca-149">X</span><span class="sxs-lookup"><span data-stu-id="421ca-149">X</span></span>   |            |
| <span data-ttu-id="421ca-150">Voix Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="421ca-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="421ca-151">X</span><span class="sxs-lookup"><span data-stu-id="421ca-151">X</span></span>   |            |     |            |
| <span data-ttu-id="421ca-152">Windows Media Audio professionnel</span><span class="sxs-lookup"><span data-stu-id="421ca-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="421ca-153">X</span><span class="sxs-lookup"><span data-stu-id="421ca-153">X</span></span>   | <span data-ttu-id="421ca-154">X</span><span class="sxs-lookup"><span data-stu-id="421ca-154">X</span></span>          | <span data-ttu-id="421ca-155">X</span><span class="sxs-lookup"><span data-stu-id="421ca-155">X</span></span>   | <span data-ttu-id="421ca-156">X</span><span class="sxs-lookup"><span data-stu-id="421ca-156">X</span></span>          |
| <span data-ttu-id="421ca-157">Windows Media Audio sans perte</span><span class="sxs-lookup"><span data-stu-id="421ca-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="421ca-158">X</span><span class="sxs-lookup"><span data-stu-id="421ca-158">X</span></span>   |            |
| <span data-ttu-id="421ca-159">Image Windows Media Video 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="421ca-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="421ca-160">X</span><span class="sxs-lookup"><span data-stu-id="421ca-160">X</span></span>   |            | <span data-ttu-id="421ca-161">X</span><span class="sxs-lookup"><span data-stu-id="421ca-161">X</span></span>   |            |
| <span data-ttu-id="421ca-162">Profil avancé Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="421ca-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="421ca-163">X</span><span class="sxs-lookup"><span data-stu-id="421ca-163">X</span></span>   | <span data-ttu-id="421ca-164">X</span><span class="sxs-lookup"><span data-stu-id="421ca-164">X</span></span>          | <span data-ttu-id="421ca-165">X</span><span class="sxs-lookup"><span data-stu-id="421ca-165">X</span></span>   | <span data-ttu-id="421ca-166">X</span><span class="sxs-lookup"><span data-stu-id="421ca-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="421ca-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="421ca-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="421ca-168">**Conception de profils**</span><span class="sxs-lookup"><span data-stu-id="421ca-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="421ca-169">**Encodage à débit binaire constant (CBR)**</span><span class="sxs-lookup"><span data-stu-id="421ca-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="421ca-170">**Encodage en deux passes**</span><span class="sxs-lookup"><span data-stu-id="421ca-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="421ca-171">**Encodage à vitesse de transmission variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="421ca-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




