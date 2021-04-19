---
description: Cette vue d’ensemble décrit le format RIFF (Resource Interchange File Format), qui est utilisé dans les fichiers. wav. RIFF est le format standard à partir duquel les données audio pour XAudio2 sont chargées.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535046"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="b5354-104">RIFF (Resource Interchange File Format)</span><span class="sxs-lookup"><span data-stu-id="b5354-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="b5354-105">Cette vue d’ensemble décrit le format RIFF (Resource Interchange File Format), qui est utilisé dans les fichiers. wav.</span><span class="sxs-lookup"><span data-stu-id="b5354-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="b5354-106">RIFF est le format standard à partir duquel les données audio pour XAudio2 sont chargées.</span><span class="sxs-lookup"><span data-stu-id="b5354-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="b5354-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="b5354-107">RIFF</span></span>

<span data-ttu-id="b5354-108">Un fichier RIFF est constitué de plusieurs sections discrètes de données appelées *segments*.</span><span class="sxs-lookup"><span data-stu-id="b5354-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="b5354-109">Identificateurs FOURCC</span><span class="sxs-lookup"><span data-stu-id="b5354-109">FOURCC Identifiers</span></span>

<span data-ttu-id="b5354-110">Le type de données d’un segment est indiqué par un identificateur de code à quatre caractères (FOURCC).</span><span class="sxs-lookup"><span data-stu-id="b5354-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="b5354-111">Un FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII utilisés pour identifier les types de blocs dans un fichier RIFF.</span><span class="sxs-lookup"><span data-stu-id="b5354-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="b5354-112">Par exemple, le FOURCC « ABCD » est représenté sur un système Little endian en tant que 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="b5354-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="b5354-113">FOURCCs peut contenir des espaces, « ABC » est donc un FOURCC valide.</span><span class="sxs-lookup"><span data-stu-id="b5354-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="b5354-114">Les fichiers audio utilisent des Codes FOURCC pour identifier les blocs de format audio, les segments de données audio et tout autre segment spécifique au format audio.</span><span class="sxs-lookup"><span data-stu-id="b5354-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="b5354-115">Le tableau suivant présente les identificateurs FOURCC qui peuvent être attendus dans les formats audio pris en charge par XAudio2.</span><span class="sxs-lookup"><span data-stu-id="b5354-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="b5354-116">Format</span><span class="sxs-lookup"><span data-stu-id="b5354-116">Format</span></span> | <span data-ttu-id="b5354-117">Identificateurs FOURCC</span><span class="sxs-lookup"><span data-stu-id="b5354-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="b5354-118">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b5354-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5354-119">PCM</span><span class="sxs-lookup"><span data-stu-id="b5354-119">PCM</span></span>    | <span data-ttu-id="b5354-120">« RIFF », « fmt », « données »</span><span class="sxs-lookup"><span data-stu-id="b5354-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="b5354-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="b5354-121">ADPCM</span></span>  | <span data-ttu-id="b5354-122">« RIFF », « fmt », « Data », « SMPL », « wsmpl »</span><span class="sxs-lookup"><span data-stu-id="b5354-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="b5354-123">Pour obtenir une description des identificateurs FOURCC spécifiques à ADPCM, voir [vue d’ensemble d’ADPCM](adpcm-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="b5354-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="b5354-124">Les identificateurs FOURCC « RIFF », « fmt » et « Data » sont communs à tous les formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b5354-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="b5354-125">Le tableau suivant décrit les identificateurs FOURCC qui se trouvent dans tous les formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b5354-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="b5354-126">Identificateur FOURCC</span><span class="sxs-lookup"><span data-stu-id="b5354-126">FOURCC identifier</span></span> | <span data-ttu-id="b5354-127">Description</span><span class="sxs-lookup"><span data-stu-id="b5354-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5354-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="b5354-128">"RIFF"</span></span>            | <span data-ttu-id="b5354-129">Bloc RIFF standard contenant un type de fichier avec la valeur « WAVE » ou « XWMA » dans les quatre premiers octets de sa section de données et les autres segments du fichier dans le reste de sa section de données.</span><span class="sxs-lookup"><span data-stu-id="b5354-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="b5354-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="b5354-130">"fmt"</span></span>             | <span data-ttu-id="b5354-131">Contient l’en-tête de format du fichier audio.</span><span class="sxs-lookup"><span data-stu-id="b5354-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="b5354-132">Les données de ce segment correspondent à l’une des structures suivantes : **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span><span class="sxs-lookup"><span data-stu-id="b5354-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="b5354-133">"data"</span><span class="sxs-lookup"><span data-stu-id="b5354-133">"data"</span></span>            | <span data-ttu-id="b5354-134">Contient des données audio pour le fichier audio.</span><span class="sxs-lookup"><span data-stu-id="b5354-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="b5354-135">Dans XAudio2, le contenu du segment de données est lu dans une mémoire tampon et transmis à une voix source en tant que membre **pAudioData** d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="b5354-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="b5354-136">Chunks</span><span class="sxs-lookup"><span data-stu-id="b5354-136">Chunks</span></span>

<span data-ttu-id="b5354-137">Un fichier RIFF se compose d’un bloc RIFF contenant zéro ou plusieurs autres segments.</span><span class="sxs-lookup"><span data-stu-id="b5354-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="b5354-138">Le bloc RIFF se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="b5354-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="b5354-139">« RIFF », fileSize, fileType, données</span><span class="sxs-lookup"><span data-stu-id="b5354-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="b5354-140">Où « RIFF » est le littéral de code FOURCC « RIFF », *FileSize* est une valeur de 4 octets qui donne la taille des données dans le fichier et *FILETYPE* est un FourCC qui identifie le type de fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="b5354-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="b5354-141">La valeur de *FileSize* inclut la taille du FourCC de *filetype* plus la taille des données qui suivent, mais n’inclut pas la taille du FourCC « riff » ou la taille du *FileSize*.</span><span class="sxs-lookup"><span data-stu-id="b5354-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="b5354-142">Les données se composent de segments dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="b5354-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="b5354-143">Les autres blocs se présentent sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="b5354-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="b5354-144">Où *chunkID* est un FourCC qui identifie les données contenues dans le bloc, *chunkSize* est une valeur de 4 octets qui donne la taille de la section de données du segment, et les données contiennent zéro, un ou plusieurs octets de données.</span><span class="sxs-lookup"><span data-stu-id="b5354-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="b5354-145">Les données sont toujours complétées à la limite de mot la plus proche.</span><span class="sxs-lookup"><span data-stu-id="b5354-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="b5354-146">*chunkSize* indique la taille des données valides dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="b5354-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="b5354-147">Elle n’inclut pas le remplissage, la taille de *chunkID* ou la taille de *chunkSize*.</span><span class="sxs-lookup"><span data-stu-id="b5354-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5354-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5354-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5354-149">Prise en main</span><span class="sxs-lookup"><span data-stu-id="b5354-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="b5354-150">Procédure : lire un son avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="b5354-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="b5354-151">Référence de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="b5354-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



