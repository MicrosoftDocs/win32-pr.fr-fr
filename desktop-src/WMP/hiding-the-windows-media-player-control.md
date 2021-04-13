---
title: Masquage du contrôle du lecteur Windows Media
description: Masquage du contrôle du lecteur Windows Media
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- incorporation, pages Web
- Lecteur Windows Media, masquage du contrôle ActiveX
- Windows Media Player Object Model, masquage du contrôle ActiveX
- modèle objet, masquer le contrôle ActiveX
- Windows Media Player Mobile, contrôle hidingActiveX
- Contrôle Windows Media Player ActiveX, masquage
- Windows Media Player Mobile (contrôle ActiveX), masquage
- Contrôle ActiveX, masquage
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Incorporation de page Web, masquage du contrôle ActiveX
- masquage du contrôle ActiveX du lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310769"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="ff775-126">Masquage du contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="ff775-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="ff775-127">L’objet ActiveX du lecteur Windows Media est incorporé dans une page Web à l’aide de l’élément objet.</span><span class="sxs-lookup"><span data-stu-id="ff775-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="ff775-128">Contrairement aux versions antérieures, l’élément objet qui définit le lecteur Windows Media doit être placé dans la section de corps d’une page Web, entre les balises <BODY> et </BODY> .</span><span class="sxs-lookup"><span data-stu-id="ff775-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="ff775-129">Placer l’objet Windows Media Player ActiveX dans la section HEAD d’une page Web pour masquer l’interface utilisateur peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="ff775-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="ff775-130">Si vous placez le contrôle ActiveX du lecteur Windows Media dans la section corps d’une page Web, l’interface utilisateur du contrôle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ff775-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="ff775-131">Si vous ne souhaitez pas qu’il s’affiche et que vous souhaitiez créer votre propre interface utilisateur, affectez la valeur zéro aux attributs Height et Width de l’élément objet.</span><span class="sxs-lookup"><span data-stu-id="ff775-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="ff775-132">Le contrôle peut également être rendu invisible en définissant le *lecteur*. propriété **UIMODE** sur « invisible ».</span><span class="sxs-lookup"><span data-stu-id="ff775-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="ff775-133">Pour ce faire, vous pouvez utiliser une balise PARAM comme indiqué dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="ff775-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="ff775-134">Dans ce cas, l’espace est réservé pour le contrôle à l’aide de la hauteur et de la largeur, mais rien ne s’affiche dans l’espace réservé jusqu’à ce que **UIMODE** soit remplacé par un élément autre que « invisible ».</span><span class="sxs-lookup"><span data-stu-id="ff775-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff775-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff775-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff775-136">**Utilisation du contrôle du lecteur Windows Media dans une page Web**</span><span class="sxs-lookup"><span data-stu-id="ff775-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




