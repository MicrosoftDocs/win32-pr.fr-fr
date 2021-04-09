---
title: Lecture audio simple
description: Lecture audio simple
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimédia, forme d’onde
- audio, forme d’onde
- audio Wave, lecture simple
- MessageBeep, fonction
- sndPlaySound fonction)
- PlaySound, fonction, lecture simple
- audio multimédia, fonction PlaySound
- audio, PlaySound, fonction
- Wave audio, fonction PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940911"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="c2913-112">Lecture audio simple</span><span class="sxs-lookup"><span data-stu-id="c2913-112">Simple Audio Playback</span></span>

<span data-ttu-id="c2913-113">Vous pouvez utiliser les fonctions suivantes pour lire les données audio de forme d’onde dans votre application dans un appel de fonction unique.</span><span class="sxs-lookup"><span data-stu-id="c2913-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="c2913-114">Fonction</span><span class="sxs-lookup"><span data-stu-id="c2913-114">Function</span></span>                                                      | <span data-ttu-id="c2913-115">Description</span><span class="sxs-lookup"><span data-stu-id="c2913-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2913-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="c2913-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="c2913-117">Lit le son qui correspond à un niveau d’alerte système spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2913-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="c2913-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2913-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="c2913-119">Lit le son qui correspond au son du système entré dans le registre ou le contenu du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2913-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="c2913-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2913-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="c2913-121">Fournit toutes les fonctionnalités de [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) et peut accéder directement aux ressources.</span><span class="sxs-lookup"><span data-stu-id="c2913-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="c2913-122">La fonction **MessageBeep** est une partie standard de l’API Win32. étant donné que ses fonctionnalités sont très limitées et qu’elles sont documentées ailleurs, elles ne sont pas abordées ici.</span><span class="sxs-lookup"><span data-stu-id="c2913-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="c2913-123">Les fonctions listées prennent en charge les sources audio Wave suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2913-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="c2913-124">Fichiers Waveform-Audio associés aux niveaux d’alerte système</span><span class="sxs-lookup"><span data-stu-id="c2913-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="c2913-125">Fichiers Waveform-Audio spécifiés par les entrées dans le registre</span><span class="sxs-lookup"><span data-stu-id="c2913-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="c2913-126">Ressources d’ondulation en mémoire</span><span class="sxs-lookup"><span data-stu-id="c2913-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="c2913-127">Waveform-fichiers audio spécifiés par le nom</span><span class="sxs-lookup"><span data-stu-id="c2913-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="c2913-128">Les fonctions [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) et [**PlaySound**](/previous-versions//dd743680(v=vs.85)) chargent l’intégralité d’un fichier Waveform-Audio en mémoire et limitent, en effet, la taille du fichier qu’ils peuvent lire.</span><span class="sxs-lookup"><span data-stu-id="c2913-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="c2913-129">Utilisez **sndPlaySound** et **PlaySound** pour lire des fichiers audio Waveform de petite taille, jusqu’à 100 000.</span><span class="sxs-lookup"><span data-stu-id="c2913-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="c2913-130">Ces deux fonctions nécessitent également que les données audio soient dans un format lisible par l’un des pilotes audio Wave installés, y compris le Mappeur Wave.</span><span class="sxs-lookup"><span data-stu-id="c2913-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="c2913-131">Pour les fichiers audio plus volumineux, utilisez les services MCI (Media Control Interface).</span><span class="sxs-lookup"><span data-stu-id="c2913-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="c2913-132">Pour plus d’informations, consultez [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="c2913-132">For more information, see [MCI](mci.md).</span></span>

 

 