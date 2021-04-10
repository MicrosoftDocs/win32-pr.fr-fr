---
title: Utilisation de niveaux chronométrés
description: Utilisation de niveaux chronométrés
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, tableau Frequency
- visualisations personnalisées, tableau de fréquence
- visualisations, tableau de forme d’onde
- visualisations personnalisées, tableau de forme d’onde
- visualisations, variable d’État
- visualisations personnalisées, variable d’État
- visualisations, variable timeStamp
- visualisations personnalisées, variable timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029235"
---
# <a name="using-timed-levels"></a><span data-ttu-id="2da3d-113">Utilisation de niveaux chronométrés</span><span class="sxs-lookup"><span data-stu-id="2da3d-113">Using Timed Levels</span></span>

<span data-ttu-id="2da3d-114">La structure **TimedLevel** est composée de tableaux 2 2 dimensionnels, d’une valeur d’État et d’une valeur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="2da3d-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="2da3d-115">Tableau Frequency</span><span class="sxs-lookup"><span data-stu-id="2da3d-115">Frequency Array</span></span>

<span data-ttu-id="2da3d-116">Le tableau Frequency est un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="2da3d-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="2da3d-117">La première dimension de chaque tableau correspond au canal audio stéréo (à gauche ou à droite), tandis que la seconde correspond aux niveaux de fréquence (en octets) de l’instantané, où le spectre audio est divisé en zones de 1024.</span><span class="sxs-lookup"><span data-stu-id="2da3d-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="2da3d-118">Vous pouvez récupérer les données de tableau de fréquences fournies par le lecteur Windows Media de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="2da3d-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="2da3d-119">La valeur de l’instantané est pour le canal gauche et contient la valeur de la partie la plus basse du spectre de fréquences.</span><span class="sxs-lookup"><span data-stu-id="2da3d-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="2da3d-120">Par exemple, si l’instantané a une valeur élevée, il indique que la partie 1024th la plus faible du spectre de fréquences est riche en fréquence.</span><span class="sxs-lookup"><span data-stu-id="2da3d-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="2da3d-121">La valeur zéro indique qu’il n’y A aucune valeur de fréquence faible dans cette partie du spectre pour le canal de gauche.</span><span class="sxs-lookup"><span data-stu-id="2da3d-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="2da3d-122">Si vous avez un signal Monophonic, seule la première dimension a des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="2da3d-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="2da3d-123">Si le signal n’est pas stéréo, le deuxième tableau contiendra une copie du signal mono.</span><span class="sxs-lookup"><span data-stu-id="2da3d-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="2da3d-124">Autrement dit, \[ la fréquence 0 \] \[ *n* \] et \[ la fréquence 1 \] \[ *n* \] contiennent les mêmes données, où *n* est l’index d’une cellule particulière.</span><span class="sxs-lookup"><span data-stu-id="2da3d-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="2da3d-125">Tableau de forme d’onde</span><span class="sxs-lookup"><span data-stu-id="2da3d-125">Waveform Array</span></span>

<span data-ttu-id="2da3d-126">Le tableau Waveform est également un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="2da3d-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="2da3d-127">La première dimension du tableau correspond au canal (à gauche ou à droite), tandis que la seconde correspond aux niveaux d’alimentation (en octets) de l’instantané, où la puissance audio est divisée en segments de temps contigus de 1024.</span><span class="sxs-lookup"><span data-stu-id="2da3d-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="2da3d-128">Vous pouvez récupérer les données du tableau de forme d’onde à partir du lecteur Windows Media de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="2da3d-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="2da3d-129">La valeur de l’instantané est pour le canal gauche et contient la première valeur de l’instantané quantifié des valeurs d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2da3d-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="2da3d-130">Lorsqu’un instantané est pris, il se compose de 1024 petites mesures incrémentielles de la puissance audio.</span><span class="sxs-lookup"><span data-stu-id="2da3d-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="2da3d-131">La valeur la plus basse du tableau est générée par la première mesure incrémentielle de la puissance audio.</span><span class="sxs-lookup"><span data-stu-id="2da3d-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="2da3d-132">Notez que les valeurs de l’alimentation sont mesurées de-128 à + 127, mais que les valeurs du tableau sont comprises entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="2da3d-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="2da3d-133">Si vous avez une vague Monophonic, seule la première dimension aura des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="2da3d-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="2da3d-134">Si le signal n’est pas stéréo, le deuxième tableau contiendra une copie du signal mono.</span><span class="sxs-lookup"><span data-stu-id="2da3d-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="2da3d-135">Autrement dit, la forme d’onde \[ 0 \] \[ *n* \] et la forme d’onde \[ 1 \] \[ *n* \] contiennent les mêmes données, où *n* est l’index d’une cellule particulière.</span><span class="sxs-lookup"><span data-stu-id="2da3d-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="2da3d-136">State</span><span class="sxs-lookup"><span data-stu-id="2da3d-136">State</span></span>

<span data-ttu-id="2da3d-137">La variable d’État reflète l’état de lecture audio du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2da3d-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="2da3d-138">Les valeurs d’énumération PlayerState sont</span><span class="sxs-lookup"><span data-stu-id="2da3d-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="2da3d-139">Vous pouvez utiliser cette variable pour effectuer des actions différentes en fonction de l’état de lecture audio.</span><span class="sxs-lookup"><span data-stu-id="2da3d-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="2da3d-140">Par exemple, vous pouvez lire un type de visualisation lorsque l’audio est lu et un autre quand il est arrêté.</span><span class="sxs-lookup"><span data-stu-id="2da3d-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="2da3d-141">Horodatage</span><span class="sxs-lookup"><span data-stu-id="2da3d-141">Time Stamp</span></span>

<span data-ttu-id="2da3d-142">La variable timeStamp reflète l’heure actuelle à laquelle l’instantané est pris.</span><span class="sxs-lookup"><span data-stu-id="2da3d-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="2da3d-143">Cette valeur peut être utilisée pour mesurer la fréquence à laquelle les instantanés sont pris.</span><span class="sxs-lookup"><span data-stu-id="2da3d-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="2da3d-144">Vous pouvez utiliser cette variable pour l’heure de vos animations.</span><span class="sxs-lookup"><span data-stu-id="2da3d-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="2da3d-145">Si les instantanés sont trop fréquents, vous pouvez faire en sorte que votre image s’affiche de la manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="2da3d-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da3d-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2da3d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da3d-147">**Implémentation du rendu**</span><span class="sxs-lookup"><span data-stu-id="2da3d-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




