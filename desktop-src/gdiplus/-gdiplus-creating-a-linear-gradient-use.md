---
description: GDI+ fournit des dégradés linéaires horizontaux, verticaux et en diagonale. Par défaut, la couleur dans un dégradé linéaire change uniformément. Toutefois, vous pouvez personnaliser un dégradé linéaire afin que la couleur change de façon non uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Création d’un dégradé linéaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563151"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="c2605-105">Création d’un dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="c2605-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="c2605-106">GDI+ fournit des dégradés linéaires horizontaux, verticaux et en diagonale.</span><span class="sxs-lookup"><span data-stu-id="c2605-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="c2605-107">Par défaut, la couleur dans un dégradé linéaire change uniformément.</span><span class="sxs-lookup"><span data-stu-id="c2605-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="c2605-108">Toutefois, vous pouvez personnaliser un dégradé linéaire afin que la couleur change de façon non uniforme.</span><span class="sxs-lookup"><span data-stu-id="c2605-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="c2605-109">Dégradés linéaires horizontaux</span><span class="sxs-lookup"><span data-stu-id="c2605-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="c2605-110">Personnalisation des dégradés linéaires</span><span class="sxs-lookup"><span data-stu-id="c2605-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="c2605-111">Dégradés linéaires en diagonale</span><span class="sxs-lookup"><span data-stu-id="c2605-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="c2605-112">Dégradés linéaires horizontaux</span><span class="sxs-lookup"><span data-stu-id="c2605-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="c2605-113">L’exemple suivant utilise un pinceau de dégradé linéaire horizontal pour remplir une ligne, une ellipse et un rectangle :</span><span class="sxs-lookup"><span data-stu-id="c2605-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="c2605-114">Le constructeur [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) reçoit quatre arguments : deux points et deux couleurs.</span><span class="sxs-lookup"><span data-stu-id="c2605-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="c2605-115">Le premier point (0, 10) est associé à la première couleur (rouge) et le deuxième point (200) est associé à la deuxième couleur (bleu).</span><span class="sxs-lookup"><span data-stu-id="c2605-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="c2605-116">Comme vous pouvez vous y attendre, la ligne dessinée de (0, 10) à (200, 10) passe progressivement du rouge au bleu.</span><span class="sxs-lookup"><span data-stu-id="c2605-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="c2605-117">Les 10s des points (50, 10) et (200) ne sont pas importants.</span><span class="sxs-lookup"><span data-stu-id="c2605-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="c2605-118">L’important est que les deux points aient la même deuxième coordonnée : la ligne qui les relie est horizontale.</span><span class="sxs-lookup"><span data-stu-id="c2605-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="c2605-119">L’ellipse et le rectangle changent également progressivement du rouge au bleu, car la coordonnée horizontale est comprise entre 0 et 200.</span><span class="sxs-lookup"><span data-stu-id="c2605-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="c2605-120">L’illustration suivante montre la ligne, l’ellipse et le rectangle.</span><span class="sxs-lookup"><span data-stu-id="c2605-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="c2605-121">Notez que le dégradé de couleur se répète, car la coordonnée horizontale augmente au-delà de 200.</span><span class="sxs-lookup"><span data-stu-id="c2605-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![Illustration montrant un dégradé horizontal qui remplit une ligne et une ellipse, et un rectangle qui est plus long que l’ellipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="c2605-123">Personnalisation des dégradés linéaires</span><span class="sxs-lookup"><span data-stu-id="c2605-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="c2605-124">Dans l’exemple précédent, les composants de couleur changent de manière linéaire à mesure que vous passez d’une coordonnée horizontale de 0 à une coordonnée horizontale de 200.</span><span class="sxs-lookup"><span data-stu-id="c2605-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="c2605-125">Par exemple, un point dont la première coordonnée est à mi-chemin entre 0 et 200 aura un composant bleu qui se trouve à mi-chemin entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="c2605-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="c2605-126">GDI+ vous permet d’ajuster la façon dont une couleur varie d’un bord d’un dégradé à l’autre.</span><span class="sxs-lookup"><span data-stu-id="c2605-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="c2605-127">Supposons que vous souhaitiez créer un pinceau de dégradé qui passe du noir au rouge, conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c2605-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="c2605-128">Coordonnée horizontale</span><span class="sxs-lookup"><span data-stu-id="c2605-128">Horizontal coordinate</span></span> | <span data-ttu-id="c2605-129">Composants RGB</span><span class="sxs-lookup"><span data-stu-id="c2605-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="c2605-130">0</span><span class="sxs-lookup"><span data-stu-id="c2605-130">0</span></span>                     | <span data-ttu-id="c2605-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c2605-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="c2605-132">40</span><span class="sxs-lookup"><span data-stu-id="c2605-132">40</span></span>                    | <span data-ttu-id="c2605-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c2605-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="c2605-134">200</span><span class="sxs-lookup"><span data-stu-id="c2605-134">200</span></span>                   | <span data-ttu-id="c2605-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c2605-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="c2605-136">Notez que le composant rouge est à demi-intensité lorsque la coordonnée horizontale est seulement de 20% de la façon de 0 à 200.</span><span class="sxs-lookup"><span data-stu-id="c2605-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="c2605-137">L’exemple suivant appelle la méthode [**LinearGradientBrush :: SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) d’un objet [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) pour associer trois intensités relatives à trois positions relatives.</span><span class="sxs-lookup"><span data-stu-id="c2605-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="c2605-138">Comme dans le tableau précédent, une intensité relative de 0,5 est associée à une position relative de 0,2.</span><span class="sxs-lookup"><span data-stu-id="c2605-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="c2605-139">Le code remplit une ellipse et un rectangle avec le pinceau de dégradé.</span><span class="sxs-lookup"><span data-stu-id="c2605-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="c2605-140">L’illustration suivante montre l’ellipse et le rectangle qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="c2605-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![Illustration montrant un dégradé horizontal qui remplit une ellipse et un rectangle plus long que l’ellipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="c2605-142">Dégradés linéaires en diagonale</span><span class="sxs-lookup"><span data-stu-id="c2605-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="c2605-143">Les dégradés dans les exemples précédents ont été horizontaux ; autrement dit, la couleur change progressivement au fur et à mesure que vous déplacez le long d’une ligne horizontale.</span><span class="sxs-lookup"><span data-stu-id="c2605-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="c2605-144">Vous pouvez également définir des dégradés verticaux et des dégradés en diagonale.</span><span class="sxs-lookup"><span data-stu-id="c2605-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="c2605-145">Le code suivant passe les points (0,0) et (200, 100) à un constructeur [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="c2605-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="c2605-146">La couleur bleue est associée à (0, 0) et la couleur verte est associée à (200, 100).</span><span class="sxs-lookup"><span data-stu-id="c2605-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="c2605-147">Une ligne (avec la largeur du stylet 10) et une ellipse sont remplies avec le pinceau dégradé linéaire.</span><span class="sxs-lookup"><span data-stu-id="c2605-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="c2605-148">L’illustration suivante montre la ligne et l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="c2605-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="c2605-149">Notez que la couleur de l’ellipse change graduellement à mesure que vous déplacez le long de la ligne qui est parallèle à la ligne passant par (0, 0) et (200, 100).</span><span class="sxs-lookup"><span data-stu-id="c2605-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![Illustration montrant un dégradé Diagonal qui remplit une ellipse et une ligne diagonale](images/lineargradient3.png)

 

 



