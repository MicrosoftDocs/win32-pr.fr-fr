---
title: Modes de couleurs OpenGL et gestion de la palette Windows
description: L’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données de pixels de couleur RVBA et les modes d’index de couleurs. Windows propose deux méthodes de gestion des couleurs et des palettes de couleurs vraies.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL sur Windows, modes de couleur
- OpenGL sur Windows, gestion de palette
- gestion de la palette OpenGL
- modes de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309789"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a><span data-ttu-id="cd182-108">Modes de couleurs OpenGL et gestion de la palette Windows</span><span class="sxs-lookup"><span data-stu-id="cd182-108">OpenGL Color Modes and Windows Palette Management</span></span>

<span data-ttu-id="cd182-109">L’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données en pixels de couleur : RVBA et les modes d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="cd182-109">The Microsoft implementation of OpenGL in Windows supports two color pixel data modes: RGBA and color-index modes.</span></span> <span data-ttu-id="cd182-110">Windows propose deux méthodes de gestion des couleurs analogues : la véritable gestion des couleurs et des palettes.</span><span class="sxs-lookup"><span data-stu-id="cd182-110">Windows provide two analogous ways of handling color: true color and palette management.</span></span>

<span data-ttu-id="cd182-111">Les périphériques de couleur vraies, capables d’accepter 16, 24 ou plus d’informations de couleur par pixel, peuvent afficher des dizaines de milliers, des dizaines de millions ou plus de couleurs simultanément.</span><span class="sxs-lookup"><span data-stu-id="cd182-111">True-color devices, able to accept 16, 24, or more bits of color information per pixel, can display tens of thousands, tens of millions, or more colors simultaneously.</span></span> <span data-ttu-id="cd182-112">Toutefois, les complexités surviennent quand une application doit gérer le mode RVBA ou index des couleurs sur un appareil de type palette.</span><span class="sxs-lookup"><span data-stu-id="cd182-112">Complexities arise, however, when an application has to manage RGBA or color-index mode on a palette-type device.</span></span> <span data-ttu-id="cd182-113">Les appareils de type palette, tels qu’un affichage VGA de 256 couleurs, sont limités dans le nombre de couleurs qu’ils peuvent afficher simultanément.</span><span class="sxs-lookup"><span data-stu-id="cd182-113">Palette-type devices, such as a 256-color VGA display, are limited in the number of colors they can display simultaneously.</span></span> <span data-ttu-id="cd182-114">Les applications doivent gérer un certain nombre de détails délicats pour utiliser avec succès des appareils de type palette.</span><span class="sxs-lookup"><span data-stu-id="cd182-114">Applications must handle a number of tricky details to successfully use palette-type devices.</span></span> <span data-ttu-id="cd182-115">Étant donné que les programmes en mode d’index de couleurs n’utilisent pas de palette matérielle, ils sont plus difficiles à utiliser avec les périphériques de couleurs vraies que les programmes utilisant le mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="cd182-115">Because color-index mode programs don't use a hardware palette, they are more difficult to use with true-color devices than programs using the RGBA mode.</span></span>

 

 




