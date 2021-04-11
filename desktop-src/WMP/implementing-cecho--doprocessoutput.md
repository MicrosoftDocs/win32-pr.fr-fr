---
title: Implémentation de CEcho DoProcessOutput
description: Implémentation de CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Plug-ins du lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029844"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="51eb9-108">Implémentation de CEcho ::D oProcessOutput</span><span class="sxs-lookup"><span data-stu-id="51eb9-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="51eb9-109">La méthode **DoProcessOutput** effectue le traitement du signal numérique.</span><span class="sxs-lookup"><span data-stu-id="51eb9-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="51eb9-110">Il s’agit de la méthode qui apporte les modifications aux données fournies par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="51eb9-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="51eb9-111">C’est le résultat de cette méthode que vous entendrez comme un effet d’écho lorsque votre plug-in Echo Sample est terminé.</span><span class="sxs-lookup"><span data-stu-id="51eb9-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="51eb9-112">Pour cet exemple, le plug-in traitera uniquement les données audio 8 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="51eb9-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="51eb9-113">Vous devrez apporter certaines modifications à l’exemple de code de l’Assistant de plug-in pour supprimer les sections qui traitent des données audio de profondeur en bits plus élevées.</span><span class="sxs-lookup"><span data-stu-id="51eb9-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="51eb9-114">Toutefois, il est utile d’étudier ces sections, car vous pouvez décider d’ajouter votre propre implémentation d’écho pour ces formats.</span><span class="sxs-lookup"><span data-stu-id="51eb9-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="51eb9-115">Les sections suivantes détaillent les modifications que vous devez apporter au code :</span><span class="sxs-lookup"><span data-stu-id="51eb9-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="51eb9-116">Suppression du code pour traiter une valeur supérieure à 16 bits</span><span class="sxs-lookup"><span data-stu-id="51eb9-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="51eb9-117">Traitement des données audio</span><span class="sxs-lookup"><span data-stu-id="51eb9-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="51eb9-118">Variables pour effectuer le traitement</span><span class="sxs-lookup"><span data-stu-id="51eb9-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="51eb9-119">Création de l’effet Echo</span><span class="sxs-lookup"><span data-stu-id="51eb9-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="51eb9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51eb9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51eb9-121">**Exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="51eb9-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




