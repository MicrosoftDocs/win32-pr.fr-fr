---
title: Modification de la page de propriétés de l’exemple Echo
description: Modification de la page de propriétés de l’exemple Echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379818"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="f6abd-108">Modification de la page de propriétés de l’exemple Echo</span><span class="sxs-lookup"><span data-stu-id="f6abd-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="f6abd-109">L’implémentation de la page de propriétés par défaut fournie par l’Assistant de plug-in du lecteur Windows Media, exemple de plug-in DSP, contient un seul contrôle de zone d’édition qui reçoit le facteur d’échelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f6abd-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="f6abd-110">Vous devez modifier la page de propriétés pour recevoir les deux valeurs de propriété utilisées par l’exemple Echo.</span><span class="sxs-lookup"><span data-stu-id="f6abd-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="f6abd-111">Pour obtenir une vue d’ensemble des pages de propriétés du plug-in DSP, consultez [Implementing a audio DSP plug-](implementing-an-audio-dsp-plug-in.md)in.</span><span class="sxs-lookup"><span data-stu-id="f6abd-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="f6abd-112">Les sections suivantes vous guident tout au long du processus de modification de la page de propriétés de l’exemple :</span><span class="sxs-lookup"><span data-stu-id="f6abd-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="f6abd-113">Modification de la ressource de boîte de dialogue Echo</span><span class="sxs-lookup"><span data-stu-id="f6abd-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="f6abd-114">Ajout et modification des événements</span><span class="sxs-lookup"><span data-stu-id="f6abd-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="f6abd-115">Comment l’exemple Echo conserve les données</span><span class="sxs-lookup"><span data-stu-id="f6abd-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="f6abd-116">Implémentation de CEchoPropPage :: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="f6abd-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="f6abd-117">Implémentation de CEchoPropPage :: apply</span><span class="sxs-lookup"><span data-stu-id="f6abd-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="f6abd-118">Implémentation de CEcho :: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="f6abd-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="f6abd-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6abd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6abd-120">**Exemple Echo**</span><span class="sxs-lookup"><span data-stu-id="f6abd-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




