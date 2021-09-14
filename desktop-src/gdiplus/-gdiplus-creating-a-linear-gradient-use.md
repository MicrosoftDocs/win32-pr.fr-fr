---
description: GDI+ fournit des dégradés linéaires horizontaux, verticaux et en diagonale. Par défaut, la couleur dans un dégradé linéaire change uniformément. Toutefois, vous pouvez personnaliser un dégradé linéaire afin que la couleur change de façon non uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Création d’un dégradé linéaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227874"
---
# <a name="creating-a-linear-gradient"></a>Création d’un dégradé linéaire

GDI+ fournit des dégradés linéaires horizontaux, verticaux et en diagonale. Par défaut, la couleur dans un dégradé linéaire change uniformément. Toutefois, vous pouvez personnaliser un dégradé linéaire afin que la couleur change de façon non uniforme.

-   [Dégradés linéaires horizontaux](#horizontal-linear-gradients)
-   [Personnalisation des dégradés linéaires](#customizing-linear-gradients)
-   [Dégradés linéaires en diagonale](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Dégradés linéaires horizontaux

L’exemple suivant utilise un pinceau de dégradé linéaire horizontal pour remplir une ligne, une ellipse et un rectangle :


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



Le constructeur [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) reçoit quatre arguments : deux points et deux couleurs. Le premier point (0, 10) est associé à la première couleur (rouge) et le deuxième point (200) est associé à la deuxième couleur (bleu). Comme vous pouvez vous y attendre, la ligne dessinée de (0, 10) à (200, 10) passe progressivement du rouge au bleu.

Les 10s des points (50, 10) et (200) ne sont pas importants. L’important est que les deux points aient la même deuxième coordonnée : la ligne qui les relie est horizontale. L’ellipse et le rectangle changent également progressivement du rouge au bleu, car la coordonnée horizontale est comprise entre 0 et 200.

L’illustration suivante montre la ligne, l’ellipse et le rectangle. Notez que le dégradé de couleur se répète, car la coordonnée horizontale augmente au-delà de 200.

![Illustration montrant un dégradé horizontal qui remplit une ligne et une ellipse, et un rectangle qui est plus long que l’ellipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Personnalisation des dégradés linéaires

Dans l’exemple précédent, les composants de couleur changent de manière linéaire à mesure que vous passez d’une coordonnée horizontale de 0 à une coordonnée horizontale de 200. Par exemple, un point dont la première coordonnée est à mi-chemin entre 0 et 200 aura un composant bleu qui se trouve à mi-chemin entre 0 et 255.

GDI+ vous permet d’ajuster la façon dont une couleur varie d’un bord d’un dégradé à l’autre. Supposons que vous souhaitiez créer un pinceau de dégradé qui passe du noir au rouge, conformément au tableau suivant.



| Coordonnée horizontale | Composants RGB |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Notez que le composant rouge est à demi-intensité lorsque la coordonnée horizontale est seulement de 20% de la façon de 0 à 200.

L’exemple suivant appelle la méthode [**LinearGradientBrush :: SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) d’un objet [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) pour associer trois intensités relatives à trois positions relatives. Comme dans le tableau précédent, une intensité relative de 0,5 est associée à une position relative de 0,2. Le code remplit une ellipse et un rectangle avec le pinceau de dégradé.


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



L’illustration suivante montre l’ellipse et le rectangle qui en résultent.

![Illustration montrant un dégradé horizontal qui remplit une ellipse et un rectangle plus long que l’ellipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Dégradés linéaires en diagonale

Les dégradés dans les exemples précédents ont été horizontaux ; autrement dit, la couleur change progressivement au fur et à mesure que vous déplacez le long d’une ligne horizontale. Vous pouvez également définir des dégradés verticaux et des dégradés en diagonale. Le code suivant passe les points (0,0) et (200, 100) à un constructeur [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) . La couleur bleue est associée à (0, 0) et la couleur verte est associée à (200, 100). Une ligne (avec la largeur du stylet 10) et une ellipse sont remplies avec le pinceau dégradé linéaire.


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



L’illustration suivante montre la ligne et l’ellipse. Notez que la couleur de l’ellipse change graduellement à mesure que vous déplacez le long de la ligne qui est parallèle à la ligne passant par (0, 0) et (200, 100).

![Illustration montrant un dégradé Diagonal qui remplit une ellipse et une ligne diagonale](images/lineargradient3.png)

 

 



