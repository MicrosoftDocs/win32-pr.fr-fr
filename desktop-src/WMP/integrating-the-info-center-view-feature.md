---
title: Intégration de la fonctionnalité d’affichage du centre d’informations
description: Intégration de la fonctionnalité d’affichage du centre d’informations
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online stores, intégration de l’affichage du centre d’informations
- magasins en ligne, intégration de l’affichage du centre d’informations
- tapez 1 magasins en ligne, en intégrant le mode Info Center
- tapez 2 magasins en ligne, en intégrant le mode Info Center
- Magasins en ligne du lecteur Windows Media, affichage Centre d’informations
- magasins en ligne, affichage Centre d’informations
- tapez 1 magasins en ligne, affichage Centre d’informations
- type 2 magasins en ligne, affichage Centre d’informations
- intégration de l’affichage du centre d’informations
- Affichage du centre d’informations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536877"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="6baac-113">Intégration de la fonctionnalité d’affichage du centre d’informations</span><span class="sxs-lookup"><span data-stu-id="6baac-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="6baac-114">Le lecteur Windows Media permet aux utilisateurs d’ouvrir et de fermer la fonctionnalité d’affichage du centre d’informations.</span><span class="sxs-lookup"><span data-stu-id="6baac-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="6baac-115">Le mode Info Center est la fonctionnalité dans laquelle les utilisateurs s’attendent à trouver des informations riches et étendues sur du contenu multimédia numérique spécifique.</span><span class="sxs-lookup"><span data-stu-id="6baac-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="6baac-116">Lorsque l’utilisateur choisit d’ouvrir le mode Info Center, les appels du lecteur Windows Media sur le magasin de musique actuel permettent d’afficher la page Web du mode Info Center spécifiée par l’attribut **URL** de l’élément **Centre** d’informations du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="6baac-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="6baac-117">Pour récupérer des informations sur le contenu multimédia numérique en cours de lecture, vous devez incorporer une instance du contrôle du lecteur Windows Media dans votre page Web et utiliser le modèle objet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6baac-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="6baac-118">Par exemple, pour récupérer le titre, vous pouvez utiliser le code JScript suivant :</span><span class="sxs-lookup"><span data-stu-id="6baac-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="6baac-119">Instructions pour le mode Info Center</span><span class="sxs-lookup"><span data-stu-id="6baac-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="6baac-120">Lorsque vous créez votre page Web d' **affichage du centre d’informations** , suivez les instructions ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="6baac-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="6baac-121">La page doit clairement identifier la Banque en ligne qui fournit les informations.</span><span class="sxs-lookup"><span data-stu-id="6baac-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="6baac-122">Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.</span><span class="sxs-lookup"><span data-stu-id="6baac-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="6baac-123">La page doit inclure un lien vers la déclaration de confidentialité de votre société.</span><span class="sxs-lookup"><span data-stu-id="6baac-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="6baac-124">Évitez autant que possible la navigation entre les pages au sein de la fonctionnalité d’affichage du centre d’informations.</span><span class="sxs-lookup"><span data-stu-id="6baac-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="6baac-125">Vous devez accéder à votre magasin en ligne pour la plupart des activités.</span><span class="sxs-lookup"><span data-stu-id="6baac-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="6baac-126">Il est préférable de fournir des informations précieuses sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="6baac-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6baac-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6baac-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6baac-128">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="6baac-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="6baac-129">**Élément Centre d’informations**</span><span class="sxs-lookup"><span data-stu-id="6baac-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="6baac-130">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="6baac-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6baac-131">**Utilisation du contrôle du lecteur Windows Media dans une page Web**</span><span class="sxs-lookup"><span data-stu-id="6baac-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




