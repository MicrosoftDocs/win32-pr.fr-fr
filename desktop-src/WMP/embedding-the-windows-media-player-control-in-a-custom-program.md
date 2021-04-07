---
title: Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé
description: Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- incorporation, programmes personnalisés
- incorporation de programme personnalisé
- incorporation, programmes basés sur des Visual Basic
- Incorporation de programmes basés sur Visual Basic
- incorporation, utilisation manuelle des méthodes COM
- incorporation manuelle à l’aide de méthodes COM
- incorporation, programmes C++
- Incorporation de programmes C++
- incorporation, programmes Visual Studio
- Visual Studio, incorporation de programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028986"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="6ff47-120">Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé</span><span class="sxs-lookup"><span data-stu-id="6ff47-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="6ff47-121">Étant donné que le contrôle ActiveX du lecteur Windows Media est basé sur la technologie COM (Component Object Model) Microsoft, vous pouvez l’incorporer dans des programmes écrits avec de nombreux langages de programmation différents.</span><span class="sxs-lookup"><span data-stu-id="6ff47-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="6ff47-122">Le contrôle du lecteur Windows Media représente un moyen simple d’ajouter des fonctionnalités multimédias numériques sophistiquées à n’importe quel programme.</span><span class="sxs-lookup"><span data-stu-id="6ff47-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="6ff47-123">Dans Microsoft Visual Basic, vous pouvez ajouter le contrôle à la boîte à outils du contrôle, le placer dans un formulaire et ajuster les propriétés du contrôle dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ff47-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="6ff47-124">Si vous souhaitez une interface utilisateur personnalisée, vous pouvez placer des boutons de commande sur le formulaire et ajouter du code qui gère le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6ff47-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="6ff47-125">L’incorporation du contrôle dans un programme Visual Basic est très similaire à son incorporation dans un document Office et à sa programmation avec VBA.</span><span class="sxs-lookup"><span data-stu-id="6ff47-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="6ff47-126">Vous pouvez également incorporer manuellement le contrôle à l’aide de méthodes COM pour instancier le contrôle et accéder aux interfaces COM documentées dans [Référence du modèle objet pour C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="6ff47-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="6ff47-127">Lorsque vous incorporez le contrôle du lecteur Windows Media dans un programme C++, vous avez la possibilité d’implémenter des interfaces COM qui permettent au contrôle de s’exécuter en mode distant.</span><span class="sxs-lookup"><span data-stu-id="6ff47-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="6ff47-128">Cela signifie que le contrôle incorporé partage le même moteur de lecture que le mode complet du joueur, et les utilisateurs peuvent basculer entre le mode plein et l’état ancré sans interrompre la lecture des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="6ff47-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="6ff47-129">Vous pouvez également contrôler ce qui est affiché dans les différents volets du lecteur en mode complet lorsque vos utilisateurs basculent vers l’état non ancré.</span><span class="sxs-lookup"><span data-stu-id="6ff47-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="6ff47-130">Avec l’incorporation C++, vous avez également la possibilité d’appliquer un fichier de définition d’apparence au contrôle de lecteur incorporé.</span><span class="sxs-lookup"><span data-stu-id="6ff47-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="6ff47-131">Il s’agit d’un moyen simple de créer du code d’interface utilisateur léger que vous pouvez gérer séparément de votre code de programme principal.</span><span class="sxs-lookup"><span data-stu-id="6ff47-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="6ff47-132">Microsoft Visual Studio prend en charge l’incorporation de contrôles ActiveX, y compris le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6ff47-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="6ff47-133">Lorsque vous choisissez cette solution, Visual Studio crée un nouvel assembly d’interopérabilité de substitution pour gérer l’interopérabilité entre le .NET Framework et le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6ff47-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="6ff47-134">Visual Studio utilise l’outil .NET Framework tlbimp.exe pour créer l’assembly d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="6ff47-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="6ff47-135">Cela signifie que les signatures affichées lors de l’utilisation de la fonctionnalité IntelliSense dans Visual Studio utilisent la sémantique déterminée par la version actuelle de Tlbimp.</span><span class="sxs-lookup"><span data-stu-id="6ff47-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ff47-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ff47-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff47-137">**Incorporation du contrôle du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6ff47-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="6ff47-138">**Utilisation du contrôle du lecteur Windows Media dans un programme C++**</span><span class="sxs-lookup"><span data-stu-id="6ff47-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="6ff47-139">**Utilisation du contrôle du lecteur Windows Media dans une solution .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="6ff47-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="6ff47-140">**Utilisation du contrôle du lecteur Windows Media avec Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="6ff47-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




