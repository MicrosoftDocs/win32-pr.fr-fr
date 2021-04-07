---
title: Choix entre le mode RVBA et le mode de Color-Index
description: En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL sur Windows, mode RVBA
- OpenGL sur Windows, mode index des couleurs
- Mode RVBA OpenGL
- mode d’index de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673149"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="8c853-107">Choix entre le mode RVBA et le mode de Color-Index</span><span class="sxs-lookup"><span data-stu-id="8c853-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="8c853-108">En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.</span><span class="sxs-lookup"><span data-stu-id="8c853-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="8c853-109">Envisagez d’utiliser le mode d’index des couleurs dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="8c853-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="8c853-110">Si vous disposez d’un nombre limité de bitplanes disponibles ; le mode d’index des couleurs peut produire un ombrage moins grossier que le mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="8c853-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="8c853-111">Si vous ne vous inquiétez pas de l’utilisation de couleurs « réelles »; par exemple, en utilisant plusieurs couleurs dans une carte topographiques pour désigner des élévations relatives.</span><span class="sxs-lookup"><span data-stu-id="8c853-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="8c853-112">Lorsque vous déployez une application existante qui utilise largement le mode d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="8c853-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="8c853-113">Lorsque vous souhaitez utiliser l’animation et les effets de la carte des couleurs dans votre application.</span><span class="sxs-lookup"><span data-stu-id="8c853-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="8c853-114">(Cela n’est pas possible sur les périphériques de couleurs vraies.)</span><span class="sxs-lookup"><span data-stu-id="8c853-114">(This is not possible on true-color devices.)</span></span>

 

 




