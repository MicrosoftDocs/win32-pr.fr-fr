---
description: L’ombrage lissé est une méthode d’ombrage d’une zone avec un dégradé de couleur.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombrage lissé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203884"
---
# <a name="smooth-shading"></a><span data-ttu-id="19b5c-103">Ombrage lissé</span><span class="sxs-lookup"><span data-stu-id="19b5c-103">Smooth Shading</span></span>

<span data-ttu-id="19b5c-104">L' *ombrage lissé* est une méthode d’ombrage d’une zone avec un dégradé de couleur.</span><span class="sxs-lookup"><span data-stu-id="19b5c-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="19b5c-105">L’inclusion des informations de couleur, ainsi que des limites de la primitive de dessin, spécifie le dégradé de couleur.</span><span class="sxs-lookup"><span data-stu-id="19b5c-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="19b5c-106">GDI interpole de manière linéaire la couleur de l’intérieur de la primitive transmise sur les points de terminaison de couleur.</span><span class="sxs-lookup"><span data-stu-id="19b5c-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="19b5c-107">Les informations de couleur et de vertex sont incluses avec les informations de position dans la structure de [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .</span><span class="sxs-lookup"><span data-stu-id="19b5c-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="19b5c-108">Utilisez la fonction [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) pour remplir une structure de triangle ou de rectangle.</span><span class="sxs-lookup"><span data-stu-id="19b5c-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="19b5c-109">Pour remplir un triangle avec un ombrage lissé, appelez **GradientFill** avec les trois points de terminaison triangulaires.</span><span class="sxs-lookup"><span data-stu-id="19b5c-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="19b5c-110">Pour remplir un rectangle avec un ombrage lissé, appelez **GradientFill** avec les coordonnées de rectangle supérieur gauche et inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="19b5c-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="19b5c-111">**GradientFill** fait référence aux structures [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ rectangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)et [**\_ triangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .</span><span class="sxs-lookup"><span data-stu-id="19b5c-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="19b5c-112">Pour obtenir un exemple, consultez [dessin d’un triangle ombré](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="19b5c-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



