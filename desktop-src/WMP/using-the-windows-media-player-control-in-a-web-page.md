---
title: Utilisation du contrôle du lecteur Windows Media dans une page Web
description: Utilisation du contrôle du lecteur Windows Media dans une page Web
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
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
- Incorporation de pages Web, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197072"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="b7ab4-115">Utilisation du contrôle du lecteur Windows Media dans une page Web</span><span class="sxs-lookup"><span data-stu-id="b7ab4-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="b7ab4-116">L’incorporation du contrôle du lecteur Windows Media dans une page Web vous permet de personnaliser complètement la manière dont l’utilisateur interagit avec le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="b7ab4-117">Vous pouvez utiliser l’interface fournie par le contrôle, ou vous pouvez la masquer et afficher votre propre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="b7ab4-118">Vous pouvez spécifier plusieurs propriétés du contrôle du lecteur Windows Media à l’endroit où vous incorporez le contrôle, ou vous pouvez définir les propriétés du lecteur et appeler les méthodes de lecteur dans le code de script.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="b7ab4-119">Les sections suivantes décrivent les principes fondamentaux de l’incorporation du contrôle dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="b7ab4-120">Section</span><span class="sxs-lookup"><span data-stu-id="b7ab4-120">Section</span></span>                                                                                                        | <span data-ttu-id="b7ab4-121">Description</span><span class="sxs-lookup"><span data-stu-id="b7ab4-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7ab4-122">Masquage du contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="b7ab4-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="b7ab4-123">Décrit les options permettant de masquer le contrôle du lecteur Windows Media lorsque vous souhaitez fournir votre propre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="b7ab4-124">Éléments PARAM dans un élément OBJECT</span><span class="sxs-lookup"><span data-stu-id="b7ab4-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="b7ab4-125">Décrit comment initialiser le contrôle du lecteur Windows Media quand vous l’incorporez.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="b7ab4-126">Exemple simple de script dans une page Web</span><span class="sxs-lookup"><span data-stu-id="b7ab4-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="b7ab4-127">Décrit un exemple simple, mais complet, d’un contrôle de lecteur incorporé avec une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="b7ab4-128">Utilisation du contrôle du lecteur Windows Media avec Firefox</span><span class="sxs-lookup"><span data-stu-id="b7ab4-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="b7ab4-129">Décrit comment incorporer le contrôle du lecteur Windows Media dans une page Web afin qu’il s’affiche correctement par un navigateur Firefox.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="b7ab4-130">Utilisation de Windows Media Player avec Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="b7ab4-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="b7ab4-131">Décrit comment utiliser le contrôle du lecteur Windows Media avec Netscape 7,1 et d’autres navigateurs Web basés sur Gecko.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="b7ab4-132">Le contrôle mobile du lecteur Windows Media 10 contient des fonctionnalités basées sur un sous-ensemble des fonctionnalités fournies dans la version de bureau du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="b7ab4-133">Par conséquent, il peut être incorporé dans une page Web Pocket Internet Explorer de la même façon que le contrôle Desktop est incorporé dans une page Web Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b7ab4-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="b7ab4-134">Pour savoir si une méthode, une propriété ou un événement particulier est pris en charge pour le contrôle mobile du lecteur Windows Media 10, consultez [Référence du modèle objet pour les scripts](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="b7ab4-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b7ab4-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7ab4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7ab4-136">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="b7ab4-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




