---
title: Portage de fonctions d’anticrénelage
description: Portage de fonctions d’anticrénelage
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Portage de l’IRIS dans le GL, anticrénelage
- Portage à partir de IRIS GL, anticrénelage
- portage vers OpenGL à partir de IRIS GL, anticrénelage
- Portage OpenGL depuis IRIS GL, anticrénelage
- anticrénelage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380364"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="0edeb-108">Portage de fonctions d’anticrénelage</span><span class="sxs-lookup"><span data-stu-id="0edeb-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="0edeb-109">Dans OpenGL, le mode de sous-pixel est toujours activé, par conséquent, le sous- **Pixel** de fonction de l’iris (**true**) n’est pas nécessaire et n’a pas d’équivalent OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0edeb-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="0edeb-110">Les rubriques suivantes décrivent les aspects du Portage du code d’anticrénelage du GL d’IRIS.</span><span class="sxs-lookup"><span data-stu-id="0edeb-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="0edeb-111">Portage du code de fusion</span><span class="sxs-lookup"><span data-stu-id="0edeb-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="0edeb-112">Portage des fonctions de test afunction</span><span class="sxs-lookup"><span data-stu-id="0edeb-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="0edeb-113">Utilisation des fonctions d’anticrénelage</span><span class="sxs-lookup"><span data-stu-id="0edeb-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




