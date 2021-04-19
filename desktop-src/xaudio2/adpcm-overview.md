---
description: La modulation adaptative du code Pulse (ADPCM) est un format de compression avec perte qui est implémenté pour XAudio2 afin de fournir des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Vue d’ensemble d’ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541849"
---
# <a name="adpcm-overview"></a><span data-ttu-id="b99a3-103">Vue d’ensemble d’ADPCM</span><span class="sxs-lookup"><span data-stu-id="b99a3-103">ADPCM Overview</span></span>

<span data-ttu-id="b99a3-104">La modulation adaptative du code Pulse (ADPCM) est un format de compression avec perte qui est implémenté pour XAudio2 afin de fournir des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression.</span><span class="sxs-lookup"><span data-stu-id="b99a3-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="b99a3-105">Avec un format de compression avec perte de données, certaines données sont modifiées et perdues pendant la compression.</span><span class="sxs-lookup"><span data-stu-id="b99a3-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="b99a3-106">ADPCM peut obtenir des taux de compression allant jusqu’à 4:1.</span><span class="sxs-lookup"><span data-stu-id="b99a3-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="b99a3-107">L’implémentation d’ADPCM pour XAudio2 fournit des fonctionnalités supplémentaires pour spécifier la taille du bloc échantillon de compression.</span><span class="sxs-lookup"><span data-stu-id="b99a3-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="b99a3-108">ADPCM permet au concepteur audio de choisir un paramètre qui est un compromis approprié parmi la taille, la qualité et la résolution (pour placer des points de boucle).</span><span class="sxs-lookup"><span data-stu-id="b99a3-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="b99a3-109">XAudio2 utilise une version modifiée du codec Microsoft ADPCM qui prend en charge la mise en forme des données étendues requise pour fournir des exemples personnalisés de tailles de bloc.</span><span class="sxs-lookup"><span data-stu-id="b99a3-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="b99a3-110">Pour cette raison, les données audio XAudio2 ne peuvent pas être lues par des moteurs audio qui ne prennent pas en charge cette version du codec ADPCM.</span><span class="sxs-lookup"><span data-stu-id="b99a3-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="b99a3-111">Actuellement, la compression ADPCM est uniquement disponible pour Windows, y compris les déploiements de XNA Game Studio Express pour Windows.</span><span class="sxs-lookup"><span data-stu-id="b99a3-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="b99a3-112">Encodage ADPCM</span><span class="sxs-lookup"><span data-stu-id="b99a3-112">ADPCM Encoding</span></span>

<span data-ttu-id="b99a3-113">Les données audio sont encodées dans ADPCM à l’aide de l’outil en ligne de commande AdpcmEncode.</span><span class="sxs-lookup"><span data-stu-id="b99a3-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="b99a3-114">AdpcmEncode</span><span class="sxs-lookup"><span data-stu-id="b99a3-114">AdpcmEncode</span></span>

    <span data-ttu-id="b99a3-115">Pour encoder des fichiers audio comme ADPCM pour une utilisation avec XAudio2, utilisez l’outil de ligne de commande **AdpcmEncode** .</span><span class="sxs-lookup"><span data-stu-id="b99a3-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="b99a3-116">Décodage ADPCM</span><span class="sxs-lookup"><span data-stu-id="b99a3-116">ADPCM Decoding</span></span>

<span data-ttu-id="b99a3-117">Le décodage logiciel d’ADPCM est pris en charge dans XAudio2.</span><span class="sxs-lookup"><span data-stu-id="b99a3-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="b99a3-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="b99a3-118">XAudio2</span></span>

    <span data-ttu-id="b99a3-119">Pour utiliser des données encodées ADPCM dans XAudio2, vous devez initialiser une structure **ADPCMWAVEFORMAT** avec des valeurs spécifiques à ADPCM et la passer en tant qu’argument à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) lorsque vous créez une voix source.</span><span class="sxs-lookup"><span data-stu-id="b99a3-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="b99a3-120">Pour obtenir un exemple de chargement et de lecture d’un son dans XAudio2, consultez [Comment : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="b99a3-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="b99a3-121">SamplesPerBlock</span><span class="sxs-lookup"><span data-stu-id="b99a3-121">SamplesPerBlock</span></span>

<span data-ttu-id="b99a3-122">La compression ADPCM fonctionne en séparant la forme d’onde par des blocs et en prédisant la variation des échantillons de forme d’onde dans chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="b99a3-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="b99a3-123">La taille des blocs est mesurée en échantillons.</span><span class="sxs-lookup"><span data-stu-id="b99a3-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="b99a3-124">La plus petite taille de bloc est 32 exemples et le plus élevé est 512 échantillons.</span><span class="sxs-lookup"><span data-stu-id="b99a3-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="b99a3-125">Les blocs plus grands permettent une meilleure compression, ce qui se traduit par des fichiers de plus petite taille, mais au détriment de la qualité du son et de la résolution de l’alignement des points de boucle.</span><span class="sxs-lookup"><span data-stu-id="b99a3-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="b99a3-126">En général, la modification de la valeur SamplesPerBlock entraîne ces compromis :</span><span class="sxs-lookup"><span data-stu-id="b99a3-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="b99a3-127">Si SamplesPerBlock...</span><span class="sxs-lookup"><span data-stu-id="b99a3-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="b99a3-128">Compression de fichier</span><span class="sxs-lookup"><span data-stu-id="b99a3-128">File Compression</span></span> | <span data-ttu-id="b99a3-129">Qualité du son</span><span class="sxs-lookup"><span data-stu-id="b99a3-129">Sound Quality</span></span> | <span data-ttu-id="b99a3-130">Résolution des points de boucle</span><span class="sxs-lookup"><span data-stu-id="b99a3-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="b99a3-131">Augmentation (jusqu’à 512 max.)</span><span class="sxs-lookup"><span data-stu-id="b99a3-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="b99a3-132">Augmente</span><span class="sxs-lookup"><span data-stu-id="b99a3-132">Increases</span></span>        | <span data-ttu-id="b99a3-133">Réduis</span><span class="sxs-lookup"><span data-stu-id="b99a3-133">Decreases</span></span>     | <span data-ttu-id="b99a3-134">Réduis</span><span class="sxs-lookup"><span data-stu-id="b99a3-134">Decreases</span></span>             |
| <span data-ttu-id="b99a3-135">Diminue (jusqu’à min 32)</span><span class="sxs-lookup"><span data-stu-id="b99a3-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="b99a3-136">Réduis</span><span class="sxs-lookup"><span data-stu-id="b99a3-136">Decreases</span></span>        | <span data-ttu-id="b99a3-137">Augmente</span><span class="sxs-lookup"><span data-stu-id="b99a3-137">Increases</span></span>     | <span data-ttu-id="b99a3-138">Augmente</span><span class="sxs-lookup"><span data-stu-id="b99a3-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="b99a3-139">Restrictions</span><span class="sxs-lookup"><span data-stu-id="b99a3-139">Restrictions</span></span>

<span data-ttu-id="b99a3-140">Comme ADPCM utilise des blocs d’exemple qui sont alignés l’un après l’autre, une vague compressée avec ADPCM peut avoir un bloc partiel non terminé à sa fin.</span><span class="sxs-lookup"><span data-stu-id="b99a3-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="b99a3-141">Le décodeur ADPCM génère un silence pour le reste de ce bloc partiel, ce qui empêche l’onde de s’exécuter en boucle en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="b99a3-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="b99a3-142">La valeur du paramètre *SamplesPerBlock* affecte la résolution avec laquelle vous pouvez aligner les données Wave et les points de boucle.</span><span class="sxs-lookup"><span data-stu-id="b99a3-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="b99a3-143">Si vous essayez d’appliquer la compression à une vague non alignée, vous obtiendrez une erreur ou un avertissement selon que l’onde est utilisée dans les événements de lecture en boucle.</span><span class="sxs-lookup"><span data-stu-id="b99a3-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="b99a3-144">Vous ne pouvez pas compresser une vague utilisée dans des événements de lecture en boucle.</span><span class="sxs-lookup"><span data-stu-id="b99a3-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="b99a3-145">Supprimez-le des événements de lecture en boucle et réappliquez la compression.</span><span class="sxs-lookup"><span data-stu-id="b99a3-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="b99a3-146">Si vous utilisez l’onde exclusivement en mode non-bouclage, la restriction d’alignement de bloc de l’exemple ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="b99a3-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="b99a3-147">Structure de fichiers ADPCM</span><span class="sxs-lookup"><span data-stu-id="b99a3-147">ADPCM File Structure</span></span>

<span data-ttu-id="b99a3-148">Un fichier ADPCM est un fichier RIFF standard avec les types de blocs suivants.</span><span class="sxs-lookup"><span data-stu-id="b99a3-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="b99a3-149">Bloc FCC</span><span class="sxs-lookup"><span data-stu-id="b99a3-149">Chunk FCC</span></span>     | <span data-ttu-id="b99a3-150">Description</span><span class="sxs-lookup"><span data-stu-id="b99a3-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99a3-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="b99a3-151">RIFF</span></span>          | <span data-ttu-id="b99a3-152">Bloc RIFF standard contenant un type de fichier avec la valeur WAVE dans les quatre premiers octets de sa section de données et les autres segments du fichier dans le reste de sa section de données.</span><span class="sxs-lookup"><span data-stu-id="b99a3-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b99a3-153">fmt</span><span class="sxs-lookup"><span data-stu-id="b99a3-153">fmt</span></span>           | <span data-ttu-id="b99a3-154">Contient l’en-tête format pour le fichier ADPCM.</span><span class="sxs-lookup"><span data-stu-id="b99a3-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="b99a3-155">Les données de ce segment correspondent à une structure **ADPCMWAVEFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="b99a3-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b99a3-156">data</span><span class="sxs-lookup"><span data-stu-id="b99a3-156">data</span></span>          | <span data-ttu-id="b99a3-157">Contient les données audio ADPCM encodées.</span><span class="sxs-lookup"><span data-stu-id="b99a3-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="b99a3-158">Quand vous utilisez ADPCM dans XAudio2, vous devez lire le contenu du segment de données dans une mémoire tampon et le transmettre à une voix source en tant que membre **pAudioData** d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="b99a3-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="b99a3-159">Vous n’avez pas besoin d’échanger par octet le contenu du bloc de données.</span><span class="sxs-lookup"><span data-stu-id="b99a3-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="b99a3-160">SMPL et wsmp</span><span class="sxs-lookup"><span data-stu-id="b99a3-160">smpl and wsmp</span></span> | <span data-ttu-id="b99a3-161">Types de blocs facultatifs contenant les informations de bouclage pour le fichier ADPCM.</span><span class="sxs-lookup"><span data-stu-id="b99a3-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="b99a3-162">Lorsque vous utilisez ADPCM dans XAudio2, les valeurs contenues dans les segments SMPL ou wsmp sont utilisées pour remplir les membres **LoopBeginLoopLength** et **LoopCount** de la structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="b99a3-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="b99a3-163">Sur la Xbox 360, vous devez échanger par octet les données chargées à partir d’un bloc SMPL pour tenir compte de la différence endianness entre Windows et Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="b99a3-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b99a3-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b99a3-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b99a3-165">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="b99a3-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
