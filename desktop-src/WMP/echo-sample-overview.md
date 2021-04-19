---
title: Vue d’ensemble de l’exemple Echo
description: Vue d’ensemble de l’exemple Echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-ins du lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513479"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="81f6c-108">Vue d’ensemble de l’exemple Echo</span><span class="sxs-lookup"><span data-stu-id="81f6c-108">Echo Sample Overview</span></span>

<span data-ttu-id="81f6c-109">Ce guide crée un plug-in de lecteur Windows Media DSP qui crée un effet d’écho dans le son PCM lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="81f6c-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="81f6c-110">Les objectifs du plug-in sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="81f6c-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="81f6c-111">Le plug-in traite uniquement les données audio PCM 8 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="81f6c-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="81f6c-112">Il prend en charge un délai entre 10 millisecondes (MS) et 2000 ms (2 secondes).</span><span class="sxs-lookup"><span data-stu-id="81f6c-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="81f6c-113">Cela représente une plage pratique pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="81f6c-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="81f6c-114">Il prend en charge la combinaison du signal d’origine avec le signal de temporisation.</span><span class="sxs-lookup"><span data-stu-id="81f6c-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="81f6c-115">Il fournit une implémentation de page de propriétés qui permet à l’utilisateur de fournir une valeur pour le délai et une valeur pour le pourcentage de signal de retard par rapport au niveau de signal audio global.</span><span class="sxs-lookup"><span data-stu-id="81f6c-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="81f6c-116">Pour créer le code, modifiez l’exemple de plug-in de plug-in de l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81f6c-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="81f6c-117">L’exemple Echo n’est pas inclus dans le kit de développement logiciel (SDK) du lecteur Windows Media. Il s’agit d’un exemple que vous créez.</span><span class="sxs-lookup"><span data-stu-id="81f6c-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="81f6c-118">Pour créer l’exemple Echo, vous devez commencer par le projet par défaut à partir de l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81f6c-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="81f6c-119">Vous pouvez nommer le projet comme vous le souhaitez ; Cette documentation suppose que le projet est nommé Echo.</span><span class="sxs-lookup"><span data-stu-id="81f6c-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="81f6c-120">Pour plus d’informations sur l’utilisation de l’Assistant, consultez [génération d’un plug-in DSP](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="81f6c-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="81f6c-121">La section suivante fournit une vue d’ensemble de la façon dont l’exemple crée un effet d’écho :</span><span class="sxs-lookup"><span data-stu-id="81f6c-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="81f6c-122">Fonctionnement de l’exemple Echo</span><span class="sxs-lookup"><span data-stu-id="81f6c-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="81f6c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81f6c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f6c-124">**Exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="81f6c-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




