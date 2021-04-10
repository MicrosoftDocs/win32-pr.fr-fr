---
title: Propriétés, méthodes et événements
description: Propriétés, méthodes et événements
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, propriétés du modèle d’objet
- Windows Media Player, méthodes pour le modèle objet
- Windows Media Player, événements pour le modèle objet
- Modèle objet du lecteur Windows Media, propriétés
- Modèle objet du lecteur Windows Media, méthodes
- Modèle objet du lecteur Windows Media, événements
- modèle objet, propriétés
- modèle objet, méthodes
- modèle objet, événements
- Contrôle ActiveX du lecteur Windows Media, propriétés du modèle d’objet
- Contrôle ActiveX, propriétés du modèle objet
- Contrôle ActiveX Windows Media Player Mobile, propriétés du modèle d’objet
- Windows Media Player Mobile, propriétés du modèle d’objet
- Contrôle ActiveX du lecteur Windows Media, méthodes pour le modèle objet
- Contrôle ActiveX, méthodes pour le modèle objet
- Windows Media Player Mobile ActiveX, méthodes pour le modèle objet
- Windows Media Player Mobile, méthodes pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, événements pour le modèle objet
- Contrôle ActiveX, événements pour le modèle objet
- Contrôle ActiveX Windows Media Player Mobile, événements pour le modèle objet
- Windows Media Player Mobile, événements pour le modèle objet
- Propriétés, modèle objet du lecteur Windows Media
- méthodes, modèle objet du lecteur Windows Media
- événements, modèle objet du lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100729"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="eeafb-127">Propriétés, méthodes et événements</span><span class="sxs-lookup"><span data-stu-id="eeafb-127">Properties, Methods and Events</span></span>

<span data-ttu-id="eeafb-128">Chaque objet possède des méthodes et des propriétés qui vous permettent de programmer le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eeafb-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="eeafb-129">Une méthode est une action que l’objet peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="eeafb-129">A method is an action that the object can take.</span></span> <span data-ttu-id="eeafb-130">Une propriété est une valeur de données que vous pouvez lire ou modifier.</span><span class="sxs-lookup"><span data-stu-id="eeafb-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="eeafb-131">Par exemple, la méthode **Play** démarre le contenu en cours de lecture, tandis **que la propriété** Parate indique la fréquence d’images actuelle du contenu en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="eeafb-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="eeafb-132">En outre, l’objet **Player** déclenche des événements qui vous donnent la possibilité d’effectuer des actions à des moments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="eeafb-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="eeafb-133">Vous écrivez du code dans un gestionnaire d’événements qui s’exécutera lorsque le lecteur Windows Media déclenchera l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="eeafb-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="eeafb-134">Par exemple, vous pouvez écrire du code dans un gestionnaire d’événements **PlayStateChange** qui détermine si la modification de l’État est que le support a pris fin et, dans ce cas, affiche une boîte de dialogue demandant aux utilisateurs s’ils souhaitent relire le support.</span><span class="sxs-lookup"><span data-stu-id="eeafb-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="eeafb-135">Toutes les méthodes du modèle objet du lecteur Windows Media sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="eeafb-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="eeafb-136">Si vous appelez deux méthodes dans la même procédure, la deuxième méthode ne peut pas reposer sur la première méthode ayant terminé son action.</span><span class="sxs-lookup"><span data-stu-id="eeafb-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eeafb-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeafb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeafb-138">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="eeafb-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




