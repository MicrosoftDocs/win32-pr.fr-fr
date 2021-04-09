---
description: En mode d’ombrage plat, la pyramide suivante s’affiche avec un bord aigu entre les faces adjacentes. Toutefois, en mode d’ombrage Gouraud, les valeurs d’ombrage sont interpolées à travers la périphérie, et l’apparence finale est celle d’une surface incurvée.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparaison des modes d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111662"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="d6405-104">Comparaison des modes d’ombrage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d6405-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="d6405-105">En mode d’ombrage plat, la pyramide suivante s’affiche avec un bord aigu entre les faces adjacentes.</span><span class="sxs-lookup"><span data-stu-id="d6405-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="d6405-106">Toutefois, en mode d’ombrage Gouraud, les valeurs d’ombrage sont interpolées à travers la périphérie, et l’apparence finale est celle d’une surface incurvée.</span><span class="sxs-lookup"><span data-stu-id="d6405-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![illustration d’une pyramide avec des bords tranchants et des flèches pointant vers les normales de visage](images/shade2.png)

<span data-ttu-id="d6405-108">L’ombrage Gouraud illumine les surfaces plates plus réalistes que l’ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="d6405-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="d6405-109">Un visage dans le mode d’ombrage plat est une couleur uniforme, mais l’ombrage Gouraud permet à la lumière de tomber dans une face de manière plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="d6405-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="d6405-110">Cet effet est particulièrement évident s’il existe une source de point proche.</span><span class="sxs-lookup"><span data-stu-id="d6405-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="d6405-111">L’ombrage Gouraud lisse les bords nets entre les polygones visibles avec l’ombrage plat.</span><span class="sxs-lookup"><span data-stu-id="d6405-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="d6405-112">Toutefois, cela peut entraîner des bandes Mach, qui sont des bandes de couleur ou de lumière qui ne sont pas lissées en douceur sur les polygones adjacents.</span><span class="sxs-lookup"><span data-stu-id="d6405-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="d6405-113">Votre application peut réduire l’apparence des bandes Mach en accroissant le nombre de polygones dans un objet, en renforçant la résolution d’écran ou en renforçant la profondeur de couleur de l’application.</span><span class="sxs-lookup"><span data-stu-id="d6405-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="d6405-114">L’ombrage Gouraud peut manquer des détails.</span><span class="sxs-lookup"><span data-stu-id="d6405-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="d6405-115">Par exemple, dans l’illustration suivante, une vedette est entièrement contenue dans une face de polygone.</span><span class="sxs-lookup"><span data-stu-id="d6405-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![illustration d’une facette dans un polygone](images/gouraud.png)

<span data-ttu-id="d6405-117">Dans ce cas, l’ombrage Gouraud, qui interpole entre les sommets, ne manquera pas l’ensemble du projecteur. la face serait rendue comme si la Spotlight n’existait pas.</span><span class="sxs-lookup"><span data-stu-id="d6405-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6405-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6405-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6405-119">Ombrage</span><span class="sxs-lookup"><span data-stu-id="d6405-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



