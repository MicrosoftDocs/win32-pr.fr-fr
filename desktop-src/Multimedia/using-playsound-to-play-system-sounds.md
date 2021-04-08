---
title: Utilisation de PlaySound pour lire des sons système
description: Utilisation de PlaySound pour lire des sons système
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- Wave audio, fonction PlaySound
- audio Wave, lecture des sons système
- sons Waveform, événements sonores
- PlaySound, fonction, jouer des sons système
- PlaySound, fonction, événements sonores
- lecture des sons du système Waveform-Audio
- événements sonores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842285"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="25a07-110">Utilisation de PlaySound pour lire des sons système</span><span class="sxs-lookup"><span data-stu-id="25a07-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="25a07-111">La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) lira également des sons référencés par un nom de clé dans le registre.</span><span class="sxs-lookup"><span data-stu-id="25a07-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="25a07-112">Les utilisateurs peuvent assigner leurs propres sons à des alertes et des avertissements système, ou à des actions de l’utilisateur, comme un clic sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="25a07-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="25a07-113">Les sons associés aux alertes système et aux avertissements sont appelés des *événements sonores*.</span><span class="sxs-lookup"><span data-stu-id="25a07-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="25a07-114">Pour lire un événement sonore, appelez **PlaySound** avec le paramètre *pszSound* pointant vers une chaîne contenant le nom de l’entrée de Registre qui identifie le son.</span><span class="sxs-lookup"><span data-stu-id="25a07-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="25a07-115">Par exemple, pour lire le son associé à l’entrée « MouseClick » et attendre la fin du son avant de retourner, utilisez l’instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="25a07-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="25a07-116">Si l’entrée de Registre spécifiée ou le fichier Waveform-Audio qu’il identifie n’existe pas, ou si le fichier ne tient pas dans la mémoire disponible, **PlaySound** lit le son système par défaut.</span><span class="sxs-lookup"><span data-stu-id="25a07-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="25a07-117">Les événements sonores prédéfinis par le système peuvent varier en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="25a07-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="25a07-118">La liste suivante indique les événements sonores définis pour toutes les implémentations de l’API Win32 :</span><span class="sxs-lookup"><span data-stu-id="25a07-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="25a07-119">SystemAsterisk</span><span class="sxs-lookup"><span data-stu-id="25a07-119">SystemAsterisk</span></span>
-   <span data-ttu-id="25a07-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="25a07-120">SystemExclamation</span></span>
-   <span data-ttu-id="25a07-121">SystemExit</span><span class="sxs-lookup"><span data-stu-id="25a07-121">SystemExit</span></span>
-   <span data-ttu-id="25a07-122">SystemHand</span><span class="sxs-lookup"><span data-stu-id="25a07-122">SystemHand</span></span>
-   <span data-ttu-id="25a07-123">SystemQuestion</span><span class="sxs-lookup"><span data-stu-id="25a07-123">SystemQuestion</span></span>
-   <span data-ttu-id="25a07-124">SystemStart</span><span class="sxs-lookup"><span data-stu-id="25a07-124">SystemStart</span></span>

<span data-ttu-id="25a07-125">Si une application enregistre ses propres événements de son, l’utilisateur peut configurer l’événement son à l’aide de l’interface standard du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="25a07-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="25a07-126">L’application doit enregistrer l’événement sonore à l’aide des fonctions de Registre standard. Pour plus d’informations, consultez [Registry](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="25a07-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="25a07-127">Les entrées appartiennent à la même position dans la hiérarchie du registre que le reste des événements sonores.</span><span class="sxs-lookup"><span data-stu-id="25a07-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="25a07-128">Cette position varie en fonction de l’implémentation Win32.</span><span class="sxs-lookup"><span data-stu-id="25a07-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="25a07-129">La valeur de données appropriée varie également en fonction de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="25a07-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="25a07-130">La fonction [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) recherche toujours dans le registre un KeyName correspondant à *lpszSound* avant de tenter de charger un fichier portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="25a07-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="25a07-131">La fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) accepte les indicateurs qui spécifient l’emplacement du son.</span><span class="sxs-lookup"><span data-stu-id="25a07-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 