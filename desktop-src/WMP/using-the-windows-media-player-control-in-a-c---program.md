---
title: Utilisation du contrôle du lecteur Windows Media dans un programme C++
description: Utilisation du contrôle du lecteur Windows Media dans un programme C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, C++
- Windows Media Player Object Model, C++
- modèle objet, C++
- Windows Media Player Mobile, C++
- Contrôle ActiveX du lecteur Windows Media, C++
- Windows Media Player Mobile, contrôle ActiveX, C++
- Contrôle ActiveX, C++
- Incorporation de programmes C++
- incorporation, programmes C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197073"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="af584-119">Utilisation du contrôle du lecteur Windows Media dans un programme C++</span><span class="sxs-lookup"><span data-stu-id="af584-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="af584-120">L’utilisation de C++ pour incorporer le contrôle du lecteur Windows Media est prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="af584-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="af584-121">Il existe différentes façons d’utiliser le contrôle du lecteur Windows Media dans un programme C++.</span><span class="sxs-lookup"><span data-stu-id="af584-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="af584-122">Vous pouvez créer une instance du contrôle dans une application console, ou incorporer le contrôle dans une application Windows.</span><span class="sxs-lookup"><span data-stu-id="af584-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="af584-123">En outre, vous pouvez implémenter des interfaces qui vous permettent d’exécuter un contrôle de lecteur incorporé en mode distant.</span><span class="sxs-lookup"><span data-stu-id="af584-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="af584-124">Vous pouvez personnaliser l’interface utilisateur d’un contrôle incorporé en appliquant un fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="af584-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="af584-125">Ces informations sont décrites dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="af584-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="af584-126">Rubrique</span><span class="sxs-lookup"><span data-stu-id="af584-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="af584-127">Description</span><span class="sxs-lookup"><span data-stu-id="af584-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af584-128">Utilisation du contrôle du lecteur Windows Media dans une application console</span><span class="sxs-lookup"><span data-stu-id="af584-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="af584-129">Décrit une application console C++ simple qui instancie le contrôle du lecteur Windows Media pour afficher la version.</span><span class="sxs-lookup"><span data-stu-id="af584-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="af584-130">Hébergement du contrôle du lecteur Windows Media dans une application Windows</span><span class="sxs-lookup"><span data-stu-id="af584-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="af584-131">Décrit comment utiliser la fenêtre hôte ActiveX ATL pour incorporer le contrôle du lecteur Windows Media dans un programme Windows.</span><span class="sxs-lookup"><span data-stu-id="af584-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="af584-132">Utilisation à distance du contrôle Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="af584-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="af584-133">Décrit comment incorporer le contrôle du lecteur Windows Media dans un programme C++ en mode distant, ce qui permet à vos utilisateurs de détacher le contrôle pour basculer vers le mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="af584-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="af584-134">Gestion des événements en C++</span><span class="sxs-lookup"><span data-stu-id="af584-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="af584-135">Décrit comment recevoir des notifications d’événements à partir du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="af584-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="af584-136">Utilisation d’habillages avec le contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="af584-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="af584-137">Décrit comment appliquer un fichier d’apparence à un contrôle de lecteur Windows Media incorporé dans un programme C++.</span><span class="sxs-lookup"><span data-stu-id="af584-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="af584-138">Vous pouvez incorporer le contrôle mobile du lecteur Windows Media 10 dans une application Windows CE.</span><span class="sxs-lookup"><span data-stu-id="af584-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="af584-139">Les techniques que vous utilisez pour ce faire sont similaires à celles utilisées avec le contrôle du lecteur Windows Media du bureau.</span><span class="sxs-lookup"><span data-stu-id="af584-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="af584-140">Toutefois, il existe des différences entre ATL pour Windows et ATL pour Windows CE.</span><span class="sxs-lookup"><span data-stu-id="af584-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="af584-141">Cette documentation décrit les différences entre ces implémentations, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="af584-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="af584-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af584-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af584-143">**Référence du modèle objet pour C++**</span><span class="sxs-lookup"><span data-stu-id="af584-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="af584-144">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="af584-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




