---
title: Assistant de plug-in DSP
description: Assistant de plug-in DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-ins du lecteur Windows Media, Assistant plug-in
- plug-ins, Assistant de plug-in
- plug-ins de traitement de signal numérique, Assistant plug-in
- Plug-ins DSP, Assistant plug-in
- Assistant de plug-in
- Visual Studio, Assistant de plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507186"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="e520e-109">Assistant de plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="e520e-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="e520e-110">Le kit de développement logiciel (SDK) du lecteur Windows Media fournit un assistant de plug-in que vous pouvez ajouter à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e520e-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="e520e-111">L’Assistant peut générer un exemple de code pour différents plug-ins, y compris les types suivants de plug-ins DSP :</span><span class="sxs-lookup"><span data-stu-id="e520e-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="e520e-112">Plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="e520e-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="e520e-113">Plug-in audio DSP (mode double)</span><span class="sxs-lookup"><span data-stu-id="e520e-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="e520e-114">Plug-in de vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="e520e-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="e520e-115">Plug-in de vidéo DSP (double mode)</span><span class="sxs-lookup"><span data-stu-id="e520e-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="e520e-116">Chacun des deux exemples de plug-ins de base, DSP et Video DSP, fonctionne comme un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="e520e-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="e520e-117">Autrement dit, chaque exemple de plug-in implémente l’interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="e520e-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="e520e-118">Chacun des deux exemples de plug-ins en mode double peut fonctionner en tant qu’DMO ou en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="e520e-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="e520e-119">Autrement dit, chaque plug-in d’exemple en mode double implémente à la fois l’interface **IMediaObject** et l’interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="e520e-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="e520e-120">Vous pouvez compiler, lier, inscrire et tester l’exemple de code de plug-in.</span><span class="sxs-lookup"><span data-stu-id="e520e-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="e520e-121">Vous pouvez ensuite modifier l’exemple de code généré pour créer votre propre plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="e520e-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e520e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e520e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e520e-123">**Génération d’un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="e520e-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="e520e-124">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="e520e-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="e520e-125">**Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11**</span><span class="sxs-lookup"><span data-stu-id="e520e-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




