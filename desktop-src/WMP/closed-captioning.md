---
title: Sous-titrage
description: Sous-titrage
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Lecteur Windows Media, migration des sous-titres
- Windows Media Player Object Model, Smigrating Closed Captions
- modèle objet, migrer des sous-titres
- Windows Media Player Mobile, migration des sous-titres
- Contrôle ActiveX du lecteur Windows Media, migration des sous-titres
- Contrôle ActiveX Windows Media Player Mobile, migration des sous-titres
- Contrôle ActiveX, migration de sous-titres
- Synchronized Accessible Media Interchange (SAMI), migration des sous-titres fermés
- SAMI (Synchronized Accessible Media Interchange), migration de sous-titres fermés
- Guide de migration, SAMI (Synchronized Accessible Media Interchange)
- Guide de migration, sous-titrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101305"
---
# <a name="closed-captioning"></a><span data-ttu-id="0f8ac-121">Sous-titrage</span><span class="sxs-lookup"><span data-stu-id="0f8ac-121">Closed Captioning</span></span>

<span data-ttu-id="0f8ac-122">Le contrôle ActiveX du lecteur Windows Media 6,4 comprend un panneau d’affichage de sous-titres intégré qui, lorsqu’il est rendu visible, active les sous-titres en SAMI (Synchronized Accessible Media Interchange) et affiche le texte de la légende fermée.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="0f8ac-123">Le contrôle Windows Media Player 7 ou version ultérieure active l’affichage de sous-titres SAMI fermé à l’aide d’un **<DIV>** élément HTML.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="0f8ac-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0f8ac-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="0f8ac-125">Cette technique vous offre une flexibilité totale, car vous pouvez concevoir votre page Web pour afficher des sous-titres de manière personnalisée. l’affichage des sous-titres n’est plus nécessaire pour se trouver à un emplacement fixe adjacent à l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="0f8ac-126">Une fois que vous avez créé une zone pour afficher les sous-titres, utilisez *ClosedCaption*. propriété **captioningID** pour spécifier l’emplacement où le lecteur Windows Media effectue le rendu du texte de la légende fermée.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="0f8ac-127">Le kit de développement logiciel (SDK) du lecteur Windows Media contient un exemple fonctionnel d’un lecteur intégré qui affiche le texte de la légende fermée.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="0f8ac-128">Pour obtenir les exemples du kit de développement logiciel (SDK), téléchargez et installez le kit de développement logiciel (SDK) Windows Media Player complet à partir du site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0f8ac-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="0f8ac-129">Pour plus d’informations sur les sous-titres et le same, consultez le [site Web Microsoft Accessibility](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="0f8ac-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f8ac-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f8ac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f8ac-131">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="0f8ac-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0f8ac-132">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="0f8ac-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="0f8ac-133">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="0f8ac-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




