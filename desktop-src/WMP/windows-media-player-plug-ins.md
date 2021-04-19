---
title: Plug-ins du lecteur Windows Media
description: Plug-ins du lecteur Windows Media
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Lecteur Windows Media, plug-ins
- Plug-ins du lecteur Windows Media, à propos de
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511308"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="61a71-106">Plug-ins du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="61a71-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="61a71-107">Le lecteur Microsoft Windows Media expose des interfaces qui vous permettent d’étendre les fonctionnalités de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="61a71-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="61a71-108">Les sections suivantes décrivent les architectures de plug-in prises en charge et le processus de création d’un plug-in :</span><span class="sxs-lookup"><span data-stu-id="61a71-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="61a71-109">Section</span><span class="sxs-lookup"><span data-stu-id="61a71-109">Section</span></span>                                                                                                         | <span data-ttu-id="61a71-110">Description</span><span class="sxs-lookup"><span data-stu-id="61a71-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61a71-111">Génération d’un plug-in</span><span class="sxs-lookup"><span data-stu-id="61a71-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="61a71-112">Vous pouvez créer plusieurs types de plug-ins à l’aide de Visual Studio et de l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61a71-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="61a71-113">Visualisations personnalisées du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="61a71-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="61a71-114">Les visualisations du lecteur Windows Media sont des objets COM (Component Object Model) utilisés pour afficher l’image visuelle qui est synchronisée avec la partie audio de la lecture du média du lecteur.</span><span class="sxs-lookup"><span data-stu-id="61a71-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="61a71-115">Les visualisations personnalisées peuvent être créées à l’aide de Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="61a71-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="61a71-116">Plug-ins de l’interface utilisateur du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="61a71-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="61a71-117">Les plug-ins de l’interface utilisateur du lecteur Windows Media ajoutent de nouvelles fonctionnalités au volet de **lecture** en cours du lecteur en mode complet.</span><span class="sxs-lookup"><span data-stu-id="61a71-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="61a71-118">Vous pouvez créer des plug-ins qui utilisent la zone de visualisation, une fenêtre distincte, la zone Paramètres, la zone de métadonnées ou des plug-ins d’arrière-plan qui n’exposent aucune interface utilisateur visible.</span><span class="sxs-lookup"><span data-stu-id="61a71-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="61a71-119">Plug-ins du lecteur Windows Media DSP</span><span class="sxs-lookup"><span data-stu-id="61a71-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="61a71-120">Les plug-ins du lecteur Windows Media DSP modifient ou traitent les données audio et vidéo avant qu’il ne soit rendu par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="61a71-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="61a71-121">Les plug-ins DSP sont des objets Media Media Objects (DMO) qui se connectent au lecteur via des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="61a71-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="61a71-122">[Plug-ins de rendu du lecteur Windows Media (déconseillé)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61a71-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="61a71-123">Décoder les plug-ins de rendu de Windows Media Player (si nécessaire) et rendre les données personnalisées contenues dans un flux de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61a71-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="61a71-124">Les plug-ins de rendu sont des objets Media Media Objects (DMO) qui se connectent au lecteur via des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="61a71-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="61a71-125">Plug-ins de conversion du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="61a71-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="61a71-126">Les plug-ins de conversion du lecteur Windows Media convertissent les fichiers multimédias numériques créés à l’aide des technologies non fournies par Microsoft en ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="61a71-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="61a71-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61a71-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a71-128">**SDK du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="61a71-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 