---
title: Mixages audio dans Windows Vista
description: Mixages audio dans Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimédia, mélangeurs audio Windows Vista
- audio, mélangeurs audio Windows Vista
- mixages audio, Windows Vista
- mélangeurs, Windows Vista
- Mélangeurs audio Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104552176"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="8dafc-108">Mixages audio dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dafc-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="8dafc-109">À compter de Windows Vista, certains contrôles de mixage sont implémentés dans des logiciels plutôt que sur du matériel.</span><span class="sxs-lookup"><span data-stu-id="8dafc-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="8dafc-110">Par exemple, les contrôles de volume sont implémentés à l’aide de l’API de session audio Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="8dafc-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="8dafc-111">Ces contrôles n’affectent pas directement les paramètres matériels.</span><span class="sxs-lookup"><span data-stu-id="8dafc-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="8dafc-112">En outre, ils sont associés à une session audio spécifique au processus, de sorte que les modifications affectent l’application appelante, mais n’affectent pas les autres applications.</span><span class="sxs-lookup"><span data-stu-id="8dafc-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="8dafc-113">Chaque périphérique de point de terminaison audio dispose d’une disposition de mélangeur standard, implémentée dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="8dafc-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="8dafc-114">Chaque point de terminaison de rendu audio contient une ligne de destination qui contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8dafc-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="8dafc-115">Contrôle du volume</span><span class="sxs-lookup"><span data-stu-id="8dafc-115">Volume control</span></span>
    -   <span data-ttu-id="8dafc-116">Contrôle muet</span><span class="sxs-lookup"><span data-stu-id="8dafc-116">Mute control</span></span>
    -   <span data-ttu-id="8dafc-117">Ligne source : sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8dafc-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="8dafc-118">Ligne source : CD audio.</span><span class="sxs-lookup"><span data-stu-id="8dafc-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="8dafc-119">Chaque point de terminaison de capture audio contient une ligne de destination qui contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8dafc-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="8dafc-120">Contrôle du volume</span><span class="sxs-lookup"><span data-stu-id="8dafc-120">Volume control</span></span>
    -   <span data-ttu-id="8dafc-121">Contrôle muet</span><span class="sxs-lookup"><span data-stu-id="8dafc-121">Mute control</span></span>
    -   <span data-ttu-id="8dafc-122">Ligne source : entrée Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="8dafc-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="8dafc-123">Le type de composant dépend de l’appareil d’entrée, par exemple un microphone.</span><span class="sxs-lookup"><span data-stu-id="8dafc-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="8dafc-124">Chaque ligne source contient un contrôle de volume et un contrôle muet.</span><span class="sxs-lookup"><span data-stu-id="8dafc-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="8dafc-125">Le diagramme suivant montre les composants des points de terminaison de rendu et de capture.</span><span class="sxs-lookup"><span data-stu-id="8dafc-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![dispositions par défaut du mélangeur](images/mixer1.gif)

<span data-ttu-id="8dafc-127">Tous les contrôles d’un point de terminaison manipulent le même contrôle logiciel sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8dafc-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="8dafc-128">Par conséquent, si vous modifiez les paramètres d’un contrôle, vous recevrez une notification de modification de contrôle sur les autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="8dafc-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="8dafc-129">(Voir [**la \_ \_ \_ modification du contrôle mm MIXM**](mm-mixm-control-change.md).)</span><span class="sxs-lookup"><span data-stu-id="8dafc-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="8dafc-130">Cette disposition standard est fournie à des fins de compatibilité avec les applications existantes qui utilisent les fonctions de mixage audio.</span><span class="sxs-lookup"><span data-stu-id="8dafc-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="8dafc-131">Les nouvelles applications doivent éviter d’utiliser ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="8dafc-131">New applications should avoid using these functions.</span></span>

 

 




