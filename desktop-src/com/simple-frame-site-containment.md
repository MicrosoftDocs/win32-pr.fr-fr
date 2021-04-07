---
title: Relation contenant-contenu de site à cadre simple
description: Relation contenant-contenu de site à cadre simple
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939817"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="9c63a-103">Relation contenant-contenu de site à cadre simple</span><span class="sxs-lookup"><span data-stu-id="9c63a-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="9c63a-104">Un contrôle conteneur est un contrôle ActiveX capable de contenir d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="9c63a-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="9c63a-105">Une zone de groupe qui contient une collection de cases d’option est un exemple de contrôle conteneur.</span><span class="sxs-lookup"><span data-stu-id="9c63a-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="9c63a-106">Les contrôles de conteneur doivent définir le \_ bit d’État SIMPLEFRAME OLEMISC et doivent appeler l’implémentation [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) de son conteneur.</span><span class="sxs-lookup"><span data-stu-id="9c63a-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="9c63a-107">Un conteneur de contrôles ActiveX qui prend en charge les contrôles de conteneur doit implémenter **IsimpleFrameSite**.</span><span class="sxs-lookup"><span data-stu-id="9c63a-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="9c63a-108">CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl</span><span class="sxs-lookup"><span data-stu-id="9c63a-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c63a-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c63a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c63a-110">Catégories de composant</span><span class="sxs-lookup"><span data-stu-id="9c63a-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




