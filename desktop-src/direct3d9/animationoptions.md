---
description: Vous permet de définir les options d’animation.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111014"
---
# <a name="animationoptions"></a><span data-ttu-id="18f82-103">AnimationOptions</span><span class="sxs-lookup"><span data-stu-id="18f82-103">AnimationOptions</span></span>

<span data-ttu-id="18f82-104">Vous permet de définir les options d’animation.</span><span class="sxs-lookup"><span data-stu-id="18f82-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="18f82-105">Où :</span><span class="sxs-lookup"><span data-stu-id="18f82-105">Where:</span></span>

-   <span data-ttu-id="18f82-106">openclosed : utilisez 0 pour une animation fermée ou 1 pour une animation ouverte.</span><span class="sxs-lookup"><span data-stu-id="18f82-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="18f82-107">Par défaut, une animation est fermée.</span><span class="sxs-lookup"><span data-stu-id="18f82-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="18f82-108">positionquality : définit la qualité de position pour toutes les clés de position spécifiées.</span><span class="sxs-lookup"><span data-stu-id="18f82-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="18f82-109">Utilisez 0 pour les positions de spline ou 1 pour les positions linéaires.</span><span class="sxs-lookup"><span data-stu-id="18f82-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="18f82-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f82-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f82-111">Modèles</span><span class="sxs-lookup"><span data-stu-id="18f82-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



