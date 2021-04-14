---
title: Implémentation de DoProcessOutput
description: Implémentation de DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, DoProcessOutput
- Plug-ins DSP, DoProcessOutput
- plug-ins DSP audio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380051"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="f74af-108">Implémentation de DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="f74af-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="f74af-109">Pour traiter des données audio, vous devez effectuer plusieurs étapes dans **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="f74af-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="f74af-110">Les étapes suivantes utilisent l’exemple de code de l’Assistant de plug-in comme exemples.</span><span class="sxs-lookup"><span data-stu-id="f74af-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="f74af-111">Si vous souhaitez créer un plug-in DSP audio qui traite le contenu multimédia du même type que l’exemple de code de l’Assistant de plug-in, vous devez uniquement modifier le code de traitement réel mentionné à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="f74af-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="f74af-112">Voici toutes les étapes implémentées dans **DoProcessOutput**:</span><span class="sxs-lookup"><span data-stu-id="f74af-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="f74af-113">Si le plug-in n’est pas activé actuellement, copiez simplement les données inchangées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="f74af-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="f74af-114">Si votre plug-in convertit les données dans un format différent, vous devez également effectuer le traitement de la conversion ici.</span><span class="sxs-lookup"><span data-stu-id="f74af-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="f74af-115">Récupère un pointeur vers la structure du format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f74af-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="f74af-116">Vous devez récupérer les données de membre de cette structure, copiez donc le pointeur de *m \_ mtInput*.**pbformat** à une variable de pointeur locale d’un type qui correspond au type de structure de format.</span><span class="sxs-lookup"><span data-stu-id="f74af-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="f74af-117">L’exemple suivant stocke un pointeur vers une structure de format d’entrée **WAVEFORMATEX** :</span><span class="sxs-lookup"><span data-stu-id="f74af-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="f74af-118">Calculez le nombre d’échantillons à traiter.</span><span class="sxs-lookup"><span data-stu-id="f74af-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="f74af-119">L’exemple de code généré par l’Assistant de plug-in effectue cette étape en divisant le nombre d’octets à traiter par le membre **nBlockAlign** de la structure de format d’entrée WAVEFORMATEX, puis en multipliant le résultat par le nombre de canaux, qui était stocké dans le membre **nChannels** .</span><span class="sxs-lookup"><span data-stu-id="f74af-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="f74af-120">L’exemple suivant provient de l’exemple de code de l’Assistant de plug-in :</span><span class="sxs-lookup"><span data-stu-id="f74af-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="f74af-121">Déterminez la profondeur de bits de l’audio.</span><span class="sxs-lookup"><span data-stu-id="f74af-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="f74af-122">L’exemple de code de l’Assistant de plug-in détermine l’audio 8 bits ou 16 bits en inspectant le membre **wBitsPerSample** de la structure **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="f74af-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="f74af-123">Il utilise ensuite cette valeur dans une instruction switch pour fournir des routines de traitement distinctes pour chaque profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="f74af-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="f74af-124">Vous devrez peut-être utiliser une autre technique pour traiter d’autres types de format et de profondes de bits.</span><span class="sxs-lookup"><span data-stu-id="f74af-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="f74af-125">Créez une boucle pour parcourir les exemples audio dans la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f74af-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="f74af-126">Récupérez un exemple de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f74af-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="f74af-127">Pour ce faire, vous devez déréférencer le pointeur de données d’entrée et stocker le résultat dans une variable de type int. Pour le son 16 bits, vous devez effectuer un reconversion du pointeur d’octet vers un pointeur vers le petit pour gérer la plus grande précision de l’échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="f74af-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="f74af-128">Une fois que vous avez la valeur, vous pouvez incrémenter immédiatement le pointeur *pbInputData* pour qu’il pointe vers l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f74af-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="f74af-129">Les exemples suivants illustrent ce cas :</span><span class="sxs-lookup"><span data-stu-id="f74af-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="f74af-130">-ou-</span><span class="sxs-lookup"><span data-stu-id="f74af-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="f74af-131">Effectuez le traitement.</span><span class="sxs-lookup"><span data-stu-id="f74af-131">Perform the processing.</span></span> <span data-ttu-id="f74af-132">C’est là que vous appliquez les algorithmes qui modifient l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f74af-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="f74af-133">Voici ce que vous devez faire ici.</span><span class="sxs-lookup"><span data-stu-id="f74af-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="f74af-134">Écrire les données traitées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="f74af-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="f74af-135">Incrémentez immédiatement le pointeur vers la mémoire tampon de sortie, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f74af-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="f74af-136">Répétez la boucle jusqu’à ce que tous les échantillons aient été traités.</span><span class="sxs-lookup"><span data-stu-id="f74af-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="f74af-137">Retourne un **HRESULT** approprié.</span><span class="sxs-lookup"><span data-stu-id="f74af-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f74af-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f74af-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f74af-139">**Implémentation d’un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="f74af-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




