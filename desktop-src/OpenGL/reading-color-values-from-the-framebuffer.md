---
title: Lecture des valeurs de couleur à partir du trame
description: Lorsque vous utilisez des fonctions qui lisent les valeurs de couleur à partir du trame, n’oubliez pas les différences entre la lecture des valeurs RVBA et des valeurs d’index de couleurs sur les périphériques à couleurs vraies et sur les périphériques basés sur la palette.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL sur Windows, lecture des valeurs de couleur à partir de framebuffers
- lecture des valeurs de couleur à partir de framebuffers OpenGL
- framebuffers, lecture des valeurs de couleur OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672438"
---
# <a name="reading-color-values-from-the-framebuffer"></a><span data-ttu-id="74c47-106">Lecture des valeurs de couleur à partir du trame</span><span class="sxs-lookup"><span data-stu-id="74c47-106">Reading Color Values from the Framebuffer</span></span>

<span data-ttu-id="74c47-107">Lorsque vous utilisez des fonctions qui lisent les valeurs de couleur à partir du trame, n’oubliez pas les différences entre la lecture des valeurs RVBA et des valeurs d’index de couleurs sur les périphériques à couleurs vraies et sur les périphériques basés sur la palette.</span><span class="sxs-lookup"><span data-stu-id="74c47-107">When using functions that read back color values from the framebuffer, be aware of the differences between reading RGBA values and color-index values on true-color devices and on palette-based devices.</span></span>

<span data-ttu-id="74c47-108">Sur un appareil de couleur vraies :</span><span class="sxs-lookup"><span data-stu-id="74c47-108">On a true-color device:</span></span>

-   <span data-ttu-id="74c47-109">Les valeurs RVBA sont limitées au canal dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="74c47-109">RGBA values are limited to the channel in the device.</span></span>
-   <span data-ttu-id="74c47-110">Les valeurs d’index de couleurs sont stockées sous forme de valeurs RVBA dans le trame.</span><span class="sxs-lookup"><span data-stu-id="74c47-110">Color-index values are stored as RGBA values in the framebuffer.</span></span> <span data-ttu-id="74c47-111">Lorsque vous utilisez ces valeurs, vous devez effectuer une translation inverse de RVBA à l’index de palette logique.</span><span class="sxs-lookup"><span data-stu-id="74c47-111">When using these values, you must perform an inverse translation from RGBA to the logical palette index.</span></span> <span data-ttu-id="74c47-112">Si deux index logiques ont les mêmes valeurs RVBA, un index incorrect peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="74c47-112">If two logical indexes have the same RGBA values, the wrong index can be returned.</span></span>

<span data-ttu-id="74c47-113">Sur un appareil basé sur une palette :</span><span class="sxs-lookup"><span data-stu-id="74c47-113">On a palette-based device:</span></span>

-   <span data-ttu-id="74c47-114">Les valeurs RVBA sont lues à partir d’un index dans la palette système.</span><span class="sxs-lookup"><span data-stu-id="74c47-114">RGBA values are read from an index in the system palette.</span></span> <span data-ttu-id="74c47-115">L’index logique est obtenu à partir d’une table inverse, et les composants RVBA sont extraits.</span><span class="sxs-lookup"><span data-stu-id="74c47-115">The logical index is obtained from an inverse table, and the RGBA components are extracted.</span></span>
-   <span data-ttu-id="74c47-116">Les valeurs d’index de couleurs sont lues à partir d’un index dans la palette système et une table inverse est utilisée pour obtenir l’index de palette logique.</span><span class="sxs-lookup"><span data-stu-id="74c47-116">Color-index values are read from an index into the system palette and an inverse table is used to get the logical palette index.</span></span>

 

 




