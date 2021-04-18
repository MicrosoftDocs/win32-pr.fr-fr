---
title: Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile
description: Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins d’interface utilisateur
- Plug-ins Windows Media Player Mobile
- plug-ins, interface utilisateur
- plug-ins, Windows Media Player Mobile
- plug-ins d’interface utilisateur, Windows Media Player Mobile
- Plug-ins d’interface utilisateur, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509597"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="beda5-110">Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile</span><span class="sxs-lookup"><span data-stu-id="beda5-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="beda5-111">Le lecteur Windows Media 10 mobile utilise le même modèle de plug-in d’interface utilisateur que le lecteur Windows Media du bureau.</span><span class="sxs-lookup"><span data-stu-id="beda5-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="beda5-112">Toutefois, le lecteur Windows Media 10 mobile ne peut interagir qu’avec les plug-ins d’IU d’arrière-plan. En raison des modèles de plug-in similaires, les appels d’API qui s’appliquent aux plug-ins d’IU d’arrière-plan sur le Bureau s’appliquent également aux plug-ins d’IU d’arrière-plan sur un appareil Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="beda5-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="beda5-113">Les sections suivantes décrivent comment créer un plug-in d’interface utilisateur d’arrière-plan à l’aide du code généré par l’Assistant à partir de l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="beda5-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="beda5-114">Section</span><span class="sxs-lookup"><span data-stu-id="beda5-114">Section</span></span>                                                                | <span data-ttu-id="beda5-115">Description</span><span class="sxs-lookup"><span data-stu-id="beda5-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beda5-116">Prise en main</span><span class="sxs-lookup"><span data-stu-id="beda5-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="beda5-117">Décrit ce que vous devez installer et comment utiliser l’Assistant de plug-in du lecteur Windows Media pour faciliter l’automatisation de la création d’un plug-in d’interface utilisateur en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="beda5-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="beda5-118">Modification du code généré par l’Assistant</span><span class="sxs-lookup"><span data-stu-id="beda5-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="beda5-119">Décrit ce que vous devez modifier à partir du code généré par l’Assistant créé dans la section précédente afin qu’il fonctionne avec le lecteur Windows Media 10 mobile.</span><span class="sxs-lookup"><span data-stu-id="beda5-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="beda5-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="beda5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beda5-121">**Guide de programmation de plug-ins d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="beda5-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




