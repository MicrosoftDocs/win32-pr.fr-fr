---
title: Traitement des données audio
description: Traitement des données audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Plug-ins du lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, données audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512456"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="4b047-109">Traitement des données audio</span><span class="sxs-lookup"><span data-stu-id="4b047-109">Processing the Audio Data</span></span>

<span data-ttu-id="4b047-110">L’implémentation par défaut de **DoProcessOutput** commence par la récupération d’un pointeur vers une structure **WAVEFORMATEX** valide, exactement comme cela a été fait dans **AllocateStreamingResources**.</span><span class="sxs-lookup"><span data-stu-id="4b047-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="4b047-111">Il utilise ensuite les informations de cette structure pour calculer le nombre d’échantillons dans la mémoire tampon d’entrée en attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="4b047-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="4b047-112">Le code suivant provient de l’implémentation par défaut :</span><span class="sxs-lookup"><span data-stu-id="4b047-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="4b047-113">Ensuite, le code inspecte le membre **wBitsPerSample** pour déterminer la profondeur de bits de l’audio.</span><span class="sxs-lookup"><span data-stu-id="4b047-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="4b047-114">Cette valeur est utilisée dans une instruction switch pour fournir un traitement distinct pour les données audio 8 bits et 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4b047-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="4b047-115">Différences entre les données audio 8 bits et 16 bits</span><span class="sxs-lookup"><span data-stu-id="4b047-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="4b047-116">Il existe des différences importantes entre les fichiers audio 8 bits et 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4b047-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="4b047-117">Par conséquent, les routines de traitement pour créer l’effet ECHO sont différentes.</span><span class="sxs-lookup"><span data-stu-id="4b047-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="4b047-118">Les deux formats diffèrent des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b047-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="4b047-119">Chaque format a une taille d’échantillonnage différente : les échantillons 8 bits occupent chacun un octet de mémoire, tandis que les échantillons 16 bits occupent chacun deux octets.</span><span class="sxs-lookup"><span data-stu-id="4b047-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="4b047-120">Chaque format représente l’amplitude audio différemment.</span><span class="sxs-lookup"><span data-stu-id="4b047-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="4b047-121">l’audio 8 bits est représenté par un entier non signé avec une plage comprise entre 0 et 255 ; la valeur 128 représente un silence.</span><span class="sxs-lookup"><span data-stu-id="4b047-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="4b047-122">les données audio 16 bits sont représentées par un entier signé compris entre-32768 et 32767. la valeur zéro représente un silence.</span><span class="sxs-lookup"><span data-stu-id="4b047-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="4b047-123">Alors que le processus de création de l’effet ECHO est fondamentalement identique pour chaque format, les détails doivent différer légèrement.</span><span class="sxs-lookup"><span data-stu-id="4b047-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b047-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b047-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b047-125">**Implémentation de CEcho ::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="4b047-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




