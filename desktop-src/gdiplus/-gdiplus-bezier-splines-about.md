---
description: 'Une spline B&\# 233 ; la courbe est une courbe spécifiée par quatre points : deux points de terminaison (P1 et P2) et deux points de contrôle (C1 et C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Splines de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115270"
---
# <a name="bezier-splines"></a><span data-ttu-id="b3612-103">Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="b3612-103">Bezier Splines</span></span>

<span data-ttu-id="b3612-104">Une spline de Bézier est une courbe spécifiée par quatre points : deux points de terminaison (P1 et P2) et deux points de contrôle (C1 et C2).</span><span class="sxs-lookup"><span data-stu-id="b3612-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="b3612-105">La courbe commence à P1 et se termine à P2.</span><span class="sxs-lookup"><span data-stu-id="b3612-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="b3612-106">La courbe ne traverse pas les points de contrôle, mais les points de contrôle agissent comme des aimants, en tirant la courbe dans certaines directions et en influençant le mode de courbure de la courbe.</span><span class="sxs-lookup"><span data-stu-id="b3612-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="b3612-107">L’illustration suivante montre une courbe de Bézier avec ses points de terminaison et points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3612-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![Illustration montrant une spline de Bézier avec deux points de terminaison et deux points de contrôle](images/aboutgdip02-art11a.png)

<span data-ttu-id="b3612-109">Notez que la courbe commence à P1 et se déplace vers le point de contrôle C1.</span><span class="sxs-lookup"><span data-stu-id="b3612-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="b3612-110">La ligne tangente à la courbe à l’instant P1 est la ligne dessinée de P1 à C1.</span><span class="sxs-lookup"><span data-stu-id="b3612-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="b3612-111">Notez également que la ligne tangente au point de terminaison P2 est la ligne dessinée de C2 à P2.</span><span class="sxs-lookup"><span data-stu-id="b3612-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="b3612-112">Pour dessiner une spline de Bézier, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="b3612-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="b3612-113">L’objet **Graphics** fournit la méthode [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) , et l’objet **Pen** stocke les attributs de la courbe, tels que la largeur et la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="b3612-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="b3612-114">L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawBezier.</span><span class="sxs-lookup"><span data-stu-id="b3612-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="b3612-115">Les arguments restants passés à la méthode DrawBezier sont les points de terminaison et les points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3612-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="b3612-116">L’exemple suivant dessine une spline de Bézier avec le point de départ (0, 0), les points de contrôle (40, 20) et (80, 150) et le point de fin (100, 10).</span><span class="sxs-lookup"><span data-stu-id="b3612-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="b3612-117">L’illustration suivante montre la courbe, les points de contrôle et deux lignes tangentes.</span><span class="sxs-lookup"><span data-stu-id="b3612-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![Illustration montrant une spline de Bézier avec deux points de terminaison, deux points de contrôle et deux lignes tangentes](images/aboutgdip02-art12.png)

<span data-ttu-id="b3612-119">Les splines de Bézier ont été développées à l’origine par Pierre Bézier pour la conception dans le secteur de l’automobile.</span><span class="sxs-lookup"><span data-stu-id="b3612-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="b3612-120">Ils ont, depuis, prouvé qu’ils sont très utiles dans de nombreux types de conception assistée par ordinateur et sont également utilisés pour définir les contours de polices.</span><span class="sxs-lookup"><span data-stu-id="b3612-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="b3612-121">Les splines de Bézier peuvent générer une grande variété de formes, dont certaines sont présentées dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b3612-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![Illustration montrant trois splines de Bézier](images/aboutgdip02-art13.png)

 

 



