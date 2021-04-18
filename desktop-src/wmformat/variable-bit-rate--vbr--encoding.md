---
title: Encodage à vitesse de transmission variable (VBR)
description: Encodage à vitesse de transmission variable (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK, VBR Encoding
- Windows Media Format SDK, VBR (variable bit rate)
- Windows Media Format SDK, codage VBR basé sur la qualité
- Windows Media Format SDK, encodage VBR non restreint
- Windows Media Format SDK, encodage VBR restreint
- codecs, encodage VBR
- codecs, débit binaire variable (VBR)
- codecs, encodage VBR basé sur la qualité
- codecs, encodage VBR non restreint
- codecs, encodage VBR restreint
- Vitesse de transmission variable (VBR), à propos de
- VBR (vitesse de transmission variable), à propos de
- codage VBR basé sur la qualité, à propos de
- encodage VBR non restreint, à propos de
- encodage VBR restreint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512469"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="d9abd-118">Encodage à vitesse de transmission variable (VBR)</span><span class="sxs-lookup"><span data-stu-id="d9abd-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="d9abd-119">L’encodage VBR (variable binaire rate) est une alternative à l’encodage à débit binaire constant (CBR) et est pris en charge par certains codecs.</span><span class="sxs-lookup"><span data-stu-id="d9abd-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="d9abd-120">Lorsque l’encodage CBR s’efforce de maintenir la vitesse de transmission du média encodé, le VBR s’efforce d’obtenir la meilleure qualité possible du média encodé.</span><span class="sxs-lookup"><span data-stu-id="d9abd-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="d9abd-121">La qualité du contenu encodé est déterminée par la quantité de données perdues quand le contenu est compressé et décompressé.</span><span class="sxs-lookup"><span data-stu-id="d9abd-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="d9abd-122">De nombreux facteurs affectent la perte de données dans le processus de compression mais, en général, plus les données d'origine sont complexes, plus le taux de compression est élevé et plus la perte de détails est importante dans le processus de compression.</span><span class="sxs-lookup"><span data-stu-id="d9abd-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="d9abd-123">Il existe trois types d’encodage VBR : basés sur la qualité, sans contrainte et contraint.</span><span class="sxs-lookup"><span data-stu-id="d9abd-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="d9abd-124">Codage VBR basé sur la qualité</span><span class="sxs-lookup"><span data-stu-id="d9abd-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="d9abd-125">Le premier type d’encodage VBR est basé sur la qualité, qui utilise une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d9abd-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="d9abd-126">L’encodage VBR basé sur la qualité vous permet de spécifier un niveau de qualité pour un flux multimédia numérique au lieu d’une vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="d9abd-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="d9abd-127">Le codec encodera ensuite le contenu afin que tous les échantillons soient de qualité comparable.</span><span class="sxs-lookup"><span data-stu-id="d9abd-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="d9abd-128">Le principal avantage de l’encodage VBR basé sur la qualité est que la qualité est cohérente dans un fichier et d’un fichier à l’autre.</span><span class="sxs-lookup"><span data-stu-id="d9abd-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="d9abd-129">Par exemple, vous pouvez écrire un programme pour copier des chansons depuis des fichiers CD vers des fichiers ASF sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d9abd-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="d9abd-130">Dans ce cas, la qualité cohérente est probablement plus importante pour l’expérience de l’utilisateur final que la cohérence de la taille des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d9abd-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="d9abd-131">L’utilisation de l’encodage VBR basé sur la qualité garantit que toutes les chansons copiées sont de la même qualité.</span><span class="sxs-lookup"><span data-stu-id="d9abd-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="d9abd-132">L’inconvénient de l’encodage VBR basé sur la qualité est qu’il n’existe aucun moyen de connaître les exigences de taille ou de bande passante des médias encodés avant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="d9abd-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="d9abd-133">Cela peut rendre les fichiers codés en fonction du VBR de qualité inappropriés pour les cas où la mémoire ou la bande passante est limitée, comme les lecteurs multimédias portables ou les connexions Internet à faible bande passante.</span><span class="sxs-lookup"><span data-stu-id="d9abd-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="d9abd-134">En général, l’encodage VBR basé sur la qualité est bien adapté à la lecture locale ou aux connexions réseau à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="d9abd-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="d9abd-135">Dans ce cas, la qualité cohérente offre une meilleure expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9abd-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="d9abd-136">Encodage VBR sans contrainte</span><span class="sxs-lookup"><span data-stu-id="d9abd-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="d9abd-137">L’encodage VBR sans contrainte utilise deux passes d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d9abd-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="d9abd-138">Lorsque vous utilisez l’encodage VBR non restreint, vous spécifiez une vitesse de transmission pour le flux, comme vous le feriez avec l’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="d9abd-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="d9abd-139">Toutefois, le codec utilise cette valeur uniquement comme la vitesse de transmission moyenne pour le flux et l’encodage afin que la qualité soit aussi élevée que possible tout en conservant la moyenne.</span><span class="sxs-lookup"><span data-stu-id="d9abd-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="d9abd-140">La vitesse de transmission réelle à n’importe quel point dans le flux encodé peut varier considérablement de la valeur moyenne.</span><span class="sxs-lookup"><span data-stu-id="d9abd-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="d9abd-141">Vous ne définissez pas une fenêtre tampon pour l’encodage VBR sans contrainte comme vous le feriez pour un flux encodé CBR.</span><span class="sxs-lookup"><span data-stu-id="d9abd-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="d9abd-142">Au lieu de cela, le codec calcule la taille de la fenêtre de mémoire tampon requise en fonction des exigences des exemples encodés.</span><span class="sxs-lookup"><span data-stu-id="d9abd-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="d9abd-143">L’avantage d’un encodage VBR non restreint est que le flux compressé a la qualité la plus élevée possible tout en restant dans une bande passante moyenne prévisible.</span><span class="sxs-lookup"><span data-stu-id="d9abd-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="d9abd-144">Encodage VBR restreint</span><span class="sxs-lookup"><span data-stu-id="d9abd-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="d9abd-145">L’encodage VBR contraint est identique à l’encodage VBR non restreint, sauf que vous spécifiez une vitesse de transmission maximale et une fenêtre de mémoire tampon maximale dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d9abd-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="d9abd-146">Le codec utilise ensuite les valeurs maximales pour déterminer comment compresser les données.</span><span class="sxs-lookup"><span data-stu-id="d9abd-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="d9abd-147">Si vous définissez des valeurs maximales suffisamment élevées, l’encodage VBR contraint produira le même flux encodé comme un encodage VBR non restreint.</span><span class="sxs-lookup"><span data-stu-id="d9abd-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9abd-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9abd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9abd-149">**Choix d’une méthode d’encodage**</span><span class="sxs-lookup"><span data-stu-id="d9abd-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="d9abd-150">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="d9abd-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="d9abd-151">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="d9abd-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="d9abd-152">**Configuration de flux VBR**</span><span class="sxs-lookup"><span data-stu-id="d9abd-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="d9abd-153">**Encodage à débit binaire constant (CBR)**</span><span class="sxs-lookup"><span data-stu-id="d9abd-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="d9abd-154">**Encodage en deux passes**</span><span class="sxs-lookup"><span data-stu-id="d9abd-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="d9abd-155">**Utilisation de l’encodage Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="d9abd-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




