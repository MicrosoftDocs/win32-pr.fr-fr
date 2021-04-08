---
title: Types d’appareils
description: Types d’appareils
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674845"
---
# <a name="device-types"></a><span data-ttu-id="87577-103">Types d’appareils</span><span class="sxs-lookup"><span data-stu-id="87577-103">Device Types</span></span>

<span data-ttu-id="87577-104">MCI reconnaît un ensemble de base de *types d’appareils*.</span><span class="sxs-lookup"><span data-stu-id="87577-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="87577-105">Un type d’appareil est un ensemble de pilotes MCI qui partagent un jeu de commandes commun et sont utilisés pour contrôler des périphériques multimédias ou des fichiers de données similaires.</span><span class="sxs-lookup"><span data-stu-id="87577-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="87577-106">De nombreuses commandes MCI, telles que [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), nécessitent que vous spécifiiez un type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="87577-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="87577-107">Le tableau suivant répertorie les types de périphériques définis.</span><span class="sxs-lookup"><span data-stu-id="87577-107">The following table lists the defined device types.</span></span> <span data-ttu-id="87577-108">L’implémentation actuelle de MCI comprend des jeux de commandes pour un sous-ensemble de ces appareils.</span><span class="sxs-lookup"><span data-stu-id="87577-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="87577-109">Type d’appareil</span><span class="sxs-lookup"><span data-stu-id="87577-109">Device type</span></span>      | <span data-ttu-id="87577-110">Constante</span><span class="sxs-lookup"><span data-stu-id="87577-110">Constant</span></span>                      | <span data-ttu-id="87577-111">Description</span><span class="sxs-lookup"><span data-stu-id="87577-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="87577-112">**cdaudio**</span><span class="sxs-lookup"><span data-stu-id="87577-112">**cdaudio**</span></span>      | <span data-ttu-id="87577-113">\_ \_ CD audio MCI \_ devtype</span><span class="sxs-lookup"><span data-stu-id="87577-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="87577-114">Lecteur audio CD</span><span class="sxs-lookup"><span data-stu-id="87577-114">CD audio player</span></span>                                  |
| <span data-ttu-id="87577-115">**anciens**</span><span class="sxs-lookup"><span data-stu-id="87577-115">**dat**</span></span>          | <span data-ttu-id="87577-116">\_dat devtype \_ MCI</span><span class="sxs-lookup"><span data-stu-id="87577-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="87577-117">Lecteur de bandes audio numérique</span><span class="sxs-lookup"><span data-stu-id="87577-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="87577-118">**digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="87577-118">**digitalvideo**</span></span> | <span data-ttu-id="87577-119">\_ \_ vidéo numérique MCI \_ devtype</span><span class="sxs-lookup"><span data-stu-id="87577-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="87577-120">Vidéo numérique dans une fenêtre (non basée sur GDI)</span><span class="sxs-lookup"><span data-stu-id="87577-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="87577-121">**autres**</span><span class="sxs-lookup"><span data-stu-id="87577-121">**other**</span></span>        | <span data-ttu-id="87577-122">MCI \_ devtype \_ autre</span><span class="sxs-lookup"><span data-stu-id="87577-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="87577-123">Appareil MCI non défini</span><span class="sxs-lookup"><span data-stu-id="87577-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="87577-124">**superposition**</span><span class="sxs-lookup"><span data-stu-id="87577-124">**overlay**</span></span>      | <span data-ttu-id="87577-125">superposition MCI \_ devtype \_</span><span class="sxs-lookup"><span data-stu-id="87577-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="87577-126">Superposition d’appareil (vidéo analogique dans une fenêtre)</span><span class="sxs-lookup"><span data-stu-id="87577-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="87577-127">**scanner**</span><span class="sxs-lookup"><span data-stu-id="87577-127">**scanner**</span></span>      | <span data-ttu-id="87577-128">\_ \_ scanneur devtype MCI</span><span class="sxs-lookup"><span data-stu-id="87577-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="87577-129">Scanneur d’images</span><span class="sxs-lookup"><span data-stu-id="87577-129">Image scanner</span></span>                                    |
| <span data-ttu-id="87577-130">**sequencer**</span><span class="sxs-lookup"><span data-stu-id="87577-130">**sequencer**</span></span>    | <span data-ttu-id="87577-131">\_ \_ séquenceur MCI devtype</span><span class="sxs-lookup"><span data-stu-id="87577-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="87577-132">Séquenceur MIDI</span><span class="sxs-lookup"><span data-stu-id="87577-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="87577-133">**vidéo**</span><span class="sxs-lookup"><span data-stu-id="87577-133">**vcr**</span></span>          | <span data-ttu-id="87577-134">\_magnétoscope devtype \_ MCI</span><span class="sxs-lookup"><span data-stu-id="87577-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="87577-135">Vidéo-magnétoscope ou lecteur</span><span class="sxs-lookup"><span data-stu-id="87577-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="87577-136">**videodisc**</span><span class="sxs-lookup"><span data-stu-id="87577-136">**videodisc**</span></span>    | <span data-ttu-id="87577-137">\_VIDEODISC devtype \_ MCI</span><span class="sxs-lookup"><span data-stu-id="87577-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="87577-138">Lecteur Videodisc</span><span class="sxs-lookup"><span data-stu-id="87577-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="87577-139">**WaveAudio**</span><span class="sxs-lookup"><span data-stu-id="87577-139">**waveaudio**</span></span>    | <span data-ttu-id="87577-140">MCI \_ devtype \_ Waveform \_ audio</span><span class="sxs-lookup"><span data-stu-id="87577-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="87577-141">Périphérique audio qui lit des fichiers Waveform numérisés</span><span class="sxs-lookup"><span data-stu-id="87577-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="87577-142">Dans ce document, les noms des types d’appareils sont en gras.</span><span class="sxs-lookup"><span data-stu-id="87577-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="87577-143">Les noms de type d’appareil sont utilisés avec l’interface de chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="87577-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="87577-144">Les constantes de type appareil sont utilisées avec l’interface de message de commande.</span><span class="sxs-lookup"><span data-stu-id="87577-144">Device-type constants are used with the command-message interface.</span></span>

 

 




