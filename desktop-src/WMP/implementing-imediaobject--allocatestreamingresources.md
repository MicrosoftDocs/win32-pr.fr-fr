---
title: Implémentation de IMediaObject AllocateStreamingResources
description: Implémentation de IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Plug-ins du lecteur Windows Media, exemples de ressources de streaming d’écho
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, tampon de délai
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380071"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="7b8ef-109">Implémentation de IMediaObject :: AllocateStreamingResources</span><span class="sxs-lookup"><span data-stu-id="7b8ef-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="7b8ef-110">Dans l’exemple Echo, la méthode **AllocateStreamingResources** crée la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="7b8ef-111">Pour ce faire, il effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="7b8ef-112">Calcul de la taille de la mémoire tampon qui correspond au délai spécifié pour le type de média donné.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="7b8ef-113">Allouez une nouvelle mémoire ou réallouez la taille de la mémoire tampon si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="7b8ef-114">Appel d’une méthode qui remplit la mémoire tampon avec des valeurs représentant le silence.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="7b8ef-115">La valeur de silence est différente selon la profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="7b8ef-116">Pour le son 8 bits, le silence est représenté par la valeur hexadécimale 80 ; pour le son 16 bits, le silence est représenté par zéro.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="7b8ef-117">Calcul de la taille de la mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="7b8ef-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="7b8ef-118">Pour calculer la taille requise pour la mémoire tampon de délai, vous devez d’abord récupérer une structure **WAVEFORMATEX** qui contient des informations sur les données audio.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="7b8ef-119">L’exemple suivant récupère un pointeur vers cette structure à partir de la structure de **\_ \_ type de média DMO** d’entrée :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="7b8ef-120">Une fois que vous avez stocké un pointeur vers la structure **WAVEFORMATEX** appropriée, vous pouvez inspecter ses membres et les utiliser pour calculer la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="7b8ef-121">L’exemple de code suivant illustre ceci :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="7b8ef-122">Cet algorithme calcule la taille de la mémoire tampon en multipliant le délai, en millisecondes, du nombre d’échantillons par milliseconde, puis en multipliant le résultat par le nombre de canaux, puis en multipliant le résultat par le nombre d’octets par échantillon.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="7b8ef-123">Le nombre de canaux et le nombre d’octets par échantillon ne sont pas évidents ; elles sont encodées dans le membre nBlockAlign.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="7b8ef-124">La division par 1000 réduit la valeur nSamplesPerSec à des échantillons par milliseconde. la milliseconde est l’unité souhaitée, car le délai est exprimé en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="7b8ef-125">Allocation de la mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="7b8ef-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="7b8ef-126">Une fois que vous avez calculé les besoins en mémoire, vous pouvez allouer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="7b8ef-127">Il peut être nécessaire de supprimer la mémoire tampon, le cas échéant, par exemple lorsque l’utilisateur appelle la page de propriétés pour modifier la valeur du délai.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="7b8ef-128">Le code suivant illustre l’allocation de la mémoire tampon de délai :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="7b8ef-129">Si la mémoire tampon est correctement allouée, vous devez déplacer le pointeur mobile vers l’en-tête de la mémoire tampon, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="7b8ef-130">Remplissage de la mémoire tampon de délai avec silence</span><span class="sxs-lookup"><span data-stu-id="7b8ef-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="7b8ef-131">Il est pratique d’écrire une méthode pour remplir la mémoire tampon de délai avec des valeurs représentant le silence.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="7b8ef-132">La méthode doit recevoir le pointeur vers la structure WAVEFORMATEX valide, puis inspecter le membre wBitsPerSample pour déterminer si le son est 8 bits ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="7b8ef-133">L’exemple suivant remplit la mémoire tampon de délai avec la valeur correcte pour le silence :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="7b8ef-134">N’oubliez pas d’ajouter la déclaration anticipée pour la fonction au fichier d’en-tête Echo. h dans la section private :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="7b8ef-135">Vous devez ajouter du code à la fin de AllocateStreamingResources pour appeler cette méthode chaque fois que la mémoire tampon de délai est créée ou redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="7b8ef-136">L’exemple de code suivant passe le pointeur WAVEFORMATEX nommé pWave à la nouvelle méthode :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="7b8ef-137">Réallocation de la mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="7b8ef-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="7b8ef-138">Lorsque l’utilisateur modifie le délai d’attente à l’aide de la page de propriétés, la taille de la mémoire tampon de délai doit également être modifiée.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="7b8ef-139">Vous avez déjà ajouté le code à AllocateStreamingResources pour redimensionner la mémoire tampon, mais vous devez ajouter une ligne de code à CEcho ::p \_ délai pour appeler la méthode d’allocation de ressources chaque fois que la valeur de la propriété change.</span><span class="sxs-lookup"><span data-stu-id="7b8ef-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="7b8ef-140">Voici le code :</span><span class="sxs-lookup"><span data-stu-id="7b8ef-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="7b8ef-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b8ef-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b8ef-142">**Utilisation des ressources de streaming**</span><span class="sxs-lookup"><span data-stu-id="7b8ef-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




