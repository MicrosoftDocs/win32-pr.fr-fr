---
title: Création de l’effet Echo
description: Création de l’effet Echo
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Plug-ins du lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, création d’un effet d’écho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028648"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="57a01-109">Création de l’effet Echo</span><span class="sxs-lookup"><span data-stu-id="57a01-109">Creating the Echo Effect</span></span>

<span data-ttu-id="57a01-110">Vous devez d’abord supprimer le code de l’exemple d’assistant qui met à l’échelle l’audio.</span><span class="sxs-lookup"><span data-stu-id="57a01-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="57a01-111">Dans la section 8 bits, supprimez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="57a01-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="57a01-112">(N’oubliez pas que m \_ fScaleFactor a été remplacé par m \_ dwDelayTime.)</span><span class="sxs-lookup"><span data-stu-id="57a01-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="57a01-113">Dans la section 16 bits, supprimez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="57a01-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="57a01-114">L’implémentation de **DoProcessOutput** fournie par l’exemple de code de l’Assistant de plug-in crée une boucle while qui itère une fois pour chaque échantillon dans la mémoire tampon d’entrée fournie par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="57a01-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="57a01-115">Cette boucle fonctionne de la même façon pour les données audio 8 bits et 16 bits, bien qu’une boucle distincte soit requise pour chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="57a01-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="57a01-116">Dans chaque cas, la boucle démarre avec le test suivant :</span><span class="sxs-lookup"><span data-stu-id="57a01-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="57a01-117">Une fois à l’intérieur de la boucle, les routines de traitement sont très similaires pour les fichiers audio 8 bits et 16 bits.</span><span class="sxs-lookup"><span data-stu-id="57a01-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="57a01-118">La principale différence est que le code de la section 8 bits remplace la plage de valeurs de données par-128 par 127, puis reconvertit la plage avant d’écrire les données dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="57a01-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="57a01-119">Il est important de conserver la symétrie de la forme d’onde audio lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="57a01-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="57a01-120">Vous pouvez maintenant commencer à ajouter et à remplacer du code dans la boucle de traitement.</span><span class="sxs-lookup"><span data-stu-id="57a01-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="57a01-121">Récupérer un exemple à partir de la mémoire tampon d’entrée</span><span class="sxs-lookup"><span data-stu-id="57a01-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="57a01-122">Pendant chaque itération de la boucle, un seul échantillon est récupéré à partir de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="57a01-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="57a01-123">Pour le son 8 bits, l’échantillon est décalé vers la nouvelle plage, puis le pointeur vers la mémoire tampon d’entrée est avancé jusqu’à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="57a01-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="57a01-124">Le code suivant provient de l’Assistant de plug-in :</span><span class="sxs-lookup"><span data-stu-id="57a01-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="57a01-125">Pour le son 16 bits, le processus est le même, à l’exception de la normalisation :</span><span class="sxs-lookup"><span data-stu-id="57a01-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="57a01-126">N’oubliez pas que les pointeurs du code 16 bits ont été convertis en type **short**.</span><span class="sxs-lookup"><span data-stu-id="57a01-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="57a01-127">Récupérer un échantillon de la mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="57a01-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="57a01-128">Ensuite, récupérez un seul échantillon de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="57a01-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="57a01-129">Pour le code 8 bits, les échantillons de délai sont stockés dans leur plage Native comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="57a01-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="57a01-130">Le code suivant, que vous devez ajouter, récupère un exemple de délai 8 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="57a01-131">Pour le son 16 bits, le processus est similaire :</span><span class="sxs-lookup"><span data-stu-id="57a01-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="57a01-132">Écrire l’exemple d’entrée dans le tampon de délai</span><span class="sxs-lookup"><span data-stu-id="57a01-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="57a01-133">À présent, vous devez stocker l’exemple d’entrée dans le tampon de délai dans le même emplacement que celui à partir duquel vous avez récupéré l’exemple Delay.</span><span class="sxs-lookup"><span data-stu-id="57a01-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="57a01-134">Voici le code que vous devez ajouter pour l’audio 8 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="57a01-135">Voici le code à ajouter pour la section 16 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="57a01-136">Déplacer le pointeur de mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="57a01-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="57a01-137">Maintenant que le travail dans la mémoire tampon de délai est terminé pour cette itération, vous pouvez avancer le pointeur mobile sur la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="57a01-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="57a01-138">Si le pointeur atteint la fin de la mémoire tampon circulaire, vous devez modifier sa valeur pour qu’elle pointe vers l’en-tête de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="57a01-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="57a01-139">Pour ce faire, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="57a01-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="57a01-140">Voici le code de la section 16 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="57a01-141">Étant donné que le pointeur dans la section 16 bits est en réalité une copie de la variable membre, vous devez penser à mettre à jour la valeur dans la variable membre avec la nouvelle adresse.</span><span class="sxs-lookup"><span data-stu-id="57a01-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="57a01-142">Si vous ne le faites pas, le pointeur de mémoire tampon de délai pointera vers la tête de la mémoire tampon à plusieurs reprises et votre effet d’écho ne fonctionnera pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="57a01-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="57a01-143">Ajoutez le code suivant à la section 16 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="57a01-144">Mélanger l’exemple d’entrée avec l’exemple Delay</span><span class="sxs-lookup"><span data-stu-id="57a01-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="57a01-145">C’est là que vous utilisez les valeurs de mélange humide et à sec pour créer l’échantillon de sortie final.</span><span class="sxs-lookup"><span data-stu-id="57a01-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="57a01-146">Vous multipliez simplement chaque échantillon par la valeur à virgule flottante qui représente le pourcentage du signal final de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="57a01-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="57a01-147">Multipliez l’exemple d’entrée par la valeur stockée dans m \_ fDryMix ; multipliez l’exemple Delay par la valeur stockée dans m \_ fWetMix.</span><span class="sxs-lookup"><span data-stu-id="57a01-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="57a01-148">Ajoutez ensuite les deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="57a01-148">Then, add the two values.</span></span> <span data-ttu-id="57a01-149">Le code que vous devez ajouter est identique pour les sections 8 bits et 16 bits :</span><span class="sxs-lookup"><span data-stu-id="57a01-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="57a01-150">Écrire les données dans la mémoire tampon de sortie</span><span class="sxs-lookup"><span data-stu-id="57a01-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="57a01-151">Enfin, copiez l’échantillon mixte dans la mémoire tampon de sortie, puis avancez le pointeur de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="57a01-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="57a01-152">Pour l’audio 8 bits, l’Assistant de plug-in utilise le code suivant pour retourner l’exemple à sa plage d’origine :</span><span class="sxs-lookup"><span data-stu-id="57a01-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="57a01-153">Pour le son 16 bits, l’Assistant utilise le code suivant comme dernière étape de la boucle de traitement :</span><span class="sxs-lookup"><span data-stu-id="57a01-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="57a01-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57a01-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a01-155">**Implémentation de CEcho ::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="57a01-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




