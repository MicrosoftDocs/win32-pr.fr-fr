---
title: Plug-ins de l’interface utilisateur du lecteur Windows Media
description: Plug-ins de l’interface utilisateur du lecteur Windows Media
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Lecteur Windows Media, plug-ins
- Lecteur Windows Media, plug-ins d’interface utilisateur
- Plug-ins du lecteur Windows Media, interface utilisateur
- plug-ins, interface utilisateur
- plug-ins d’interface utilisateur, à propos de
- Plug-ins d’interface utilisateur, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510816"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="fec31-109">Plug-ins de l’interface utilisateur du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="fec31-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="fec31-110">Le lecteur Microsoft Windows Media fournit une architecture qui permet à l’utilisateur d’installer et d’activer des programmes de plug-in qui ajoutent des fonctionnalités d’interface utilisateur (IU) au mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="fec31-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="fec31-111">Un plug-in d’interface utilisateur classique peut permettre à un utilisateur d’acheter le CD contenant la piste en cours de diffusion ou d’accéder à des informations supplémentaires sur l’artiste.</span><span class="sxs-lookup"><span data-stu-id="fec31-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="fec31-112">Cette section du kit de développement logiciel (SDK) du lecteur Windows Media vous fournit les informations de programmation dont vous avez besoin pour créer votre propre plug-in d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fec31-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="fec31-113">La documentation du plug-in d’interface utilisateur est divisée en trois sections :</span><span class="sxs-lookup"><span data-stu-id="fec31-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="fec31-114">Section</span><span class="sxs-lookup"><span data-stu-id="fec31-114">Section</span></span>                                                                                            | <span data-ttu-id="fec31-115">Description</span><span class="sxs-lookup"><span data-stu-id="fec31-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fec31-116">À propos des plug-ins d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fec31-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="fec31-117">Fournit une vue d’ensemble de l’architecture utilisée pour les plug-ins d’interface utilisateur. Lisez cette section pour découvrir les concepts généraux associés à cette technologie.</span><span class="sxs-lookup"><span data-stu-id="fec31-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="fec31-118">Guide de programmation de plug-ins d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fec31-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="fec31-119">Explique ce que vous devez faire pour créer un plug-in d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fec31-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="fec31-120">Cette section contient des exemples de code et des procédures pas à pas.</span><span class="sxs-lookup"><span data-stu-id="fec31-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="fec31-121">Informations de référence sur la programmation de plug-ins d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fec31-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="fec31-122">Fournit une référence détaillée pour l’interface COM et les méthodes prises en charge par le kit de développement logiciel (SDK) du lecteur Windows Media pour les plug-ins d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fec31-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="fec31-123">Le lecteur Windows Media 10 Mobile fournit le même modèle de plug-in que le lecteur Windows Media du bureau.</span><span class="sxs-lookup"><span data-stu-id="fec31-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="fec31-124">Ce modèle de plug-in vous permet d’utiliser des plug-ins d’arrière-plan pour surveiller les événements, afficher l’état des propriétés, etc.</span><span class="sxs-lookup"><span data-stu-id="fec31-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="fec31-125">Le Guide de programmation de cette section décrit comment créer un plug-in d’IU d’arrière-plan pour le lecteur Windows Media 10 mobile à l’aide de l’Assistant de plug-in du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fec31-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fec31-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fec31-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fec31-127">**Plug-ins du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fec31-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




