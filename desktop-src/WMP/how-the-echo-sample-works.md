---
title: Fonctionnement de l’exemple Echo
description: Fonctionnement de l’exemple Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Plug-ins du lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509391"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="f79fa-108">Fonctionnement de l’exemple Echo</span><span class="sxs-lookup"><span data-stu-id="f79fa-108">How the Echo Sample Works</span></span>

<span data-ttu-id="f79fa-109">Le code crée l’effet ECHO en allouant une mémoire tampon suffisamment grande pour contenir exactement la quantité de données audio qui peuvent être rendues dans l’intervalle de temps spécifié par la valeur Delay Time.</span><span class="sxs-lookup"><span data-stu-id="f79fa-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="f79fa-110">La taille de la mémoire tampon est calculée, en octets, par la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="f79fa-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="f79fa-111">taille de la mémoire tampon = taux d’échantillonnage de délai \* / \* alignement de bloc 1000</span><span class="sxs-lookup"><span data-stu-id="f79fa-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="f79fa-112">Le délai est exprimé en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f79fa-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="f79fa-113">Le taux d’échantillonnage et les valeurs d’alignement de bloc sont fournis dans une structure WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="f79fa-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="f79fa-114">Le taux d’échantillonnage est en échantillons par seconde ; la division par 1000 donne des échantillons par milliseconde.</span><span class="sxs-lookup"><span data-stu-id="f79fa-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="f79fa-115">L’alignement du bloc est égal au produit du nombre de canaux (1 pour mono, 2 pour stéréo) et du nombre de bits par échantillon (8 ou 16) divisé par 8 (bits par octet).</span><span class="sxs-lookup"><span data-stu-id="f79fa-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="f79fa-116">En plus de la variable pointeur qui pointe vers le début de la mémoire tampon de délai, le code crée un pointeur mobile qui parcourt les données dans la mémoire tampon en synchronisation avec la boucle de traitement dans la fonction **DoProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="f79fa-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="f79fa-117">Lorsque le pointeur mobile atteint la fin de la mémoire tampon de retard, il revient à l’en-tête de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f79fa-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="f79fa-118">Une mémoire tampon utilisée de cette manière est appelée mémoire tampon circulaire.</span><span class="sxs-lookup"><span data-stu-id="f79fa-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="f79fa-119">Une fois que la mémoire tampon de délai existe et que le lecteur Windows Media a alloué une mémoire tampon d’entrée pour fournir des données audio et une mémoire tampon de sortie pour recevoir les données audio traitées, le traitement des échos se déroule comme suit :</span><span class="sxs-lookup"><span data-stu-id="f79fa-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="f79fa-120">Entrez une boucle qui autorise le traitement de chaque échantillon audio dans la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f79fa-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="f79fa-121">Récupérez un exemple de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f79fa-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="f79fa-122">Ensuite, déplacez le pointeur de la mémoire tampon d’entrée vers l’exemple suivant pour préparer l’itération de la boucle suivante.</span><span class="sxs-lookup"><span data-stu-id="f79fa-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="f79fa-123">Récupérez un exemple de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="f79fa-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="f79fa-124">Copiez l’exemple à partir de la mémoire tampon d’entrée vers le même emplacement dans la mémoire tampon de délai à partir de laquelle l’échantillon de dernier retard a été récupéré.</span><span class="sxs-lookup"><span data-stu-id="f79fa-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="f79fa-125">Déplacez le pointeur de mémoire tampon de délai vers l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f79fa-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="f79fa-126">Si le pointeur se déplace au-delà de la fin de la mémoire tampon, déplacez-le vers l’en-tête de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f79fa-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="f79fa-127">Associez l’exemple de la mémoire tampon d’entrée à l’exemple de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="f79fa-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="f79fa-128">Copiez le résultat dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="f79fa-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="f79fa-129">Ensuite, déplacez le pointeur de la mémoire tampon de sortie vers l’unité suivante pour préparer l’itération de la boucle suivante.</span><span class="sxs-lookup"><span data-stu-id="f79fa-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="f79fa-130">Répétez l’opération jusqu’à ce que tous les exemples soient traités.</span><span class="sxs-lookup"><span data-stu-id="f79fa-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="f79fa-131">Lorsqu’un exemple d’entrée récupéré à l’étape 2 est copié dans la mémoire tampon de délai de l’étape 4, il reste là jusqu’à ce que le pointeur mobile effectue un pas à pas détaillé dans la mémoire tampon de retard et finalement retourne à la même position.</span><span class="sxs-lookup"><span data-stu-id="f79fa-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="f79fa-132">Étant donné que la taille de la mémoire tampon de délai est conçue pour correspondre au délai, le temps écoulé entre l’échantillon copié dans la mémoire tampon de retard et l’échantillon récupéré une nouvelle fois est égal au délai spécifié (plus toute latence introduite par le traitement réel).</span><span class="sxs-lookup"><span data-stu-id="f79fa-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="f79fa-133">Lorsqu’un flux démarre, aucune donnée de délai n’est générée tant que le délai n’est pas écoulé.</span><span class="sxs-lookup"><span data-stu-id="f79fa-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="f79fa-134">Par conséquent, il est important que la mémoire tampon de délai contienne initialement un silence.</span><span class="sxs-lookup"><span data-stu-id="f79fa-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="f79fa-135">Si la mémoire tampon de délai contient des données aléatoires, l’utilisateur entendra un bruit blanc jusqu’à ce que le plug-in génère suffisamment de données de délai pour remplacer l’intégralité de la mémoire tampon de retard.</span><span class="sxs-lookup"><span data-stu-id="f79fa-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f79fa-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f79fa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f79fa-137">**Vue d’ensemble de l’exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="f79fa-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




