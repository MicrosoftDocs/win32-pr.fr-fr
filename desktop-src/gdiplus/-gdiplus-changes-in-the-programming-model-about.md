---
description: Les sections suivantes décrivent plusieurs façons dont la programmation avec Windows GDI+ diffère de la programmation avec Windows Graphics Device Interface (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Changements dans le modèle de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034364"
---
# <a name="changes-in-the-programming-model"></a>Changements dans le modèle de programmation

Les sections suivantes décrivent plusieurs façons dont la programmation avec Windows GDI+ diffère de la programmation avec Windows Graphics Device Interface (GDI).

-   [Contextes de périphérique, Handles et objets graphiques](#device-contexts-handles-and-graphics-objects)
-   [Deux façons de dessiner une ligne](#two-ways-to-draw-a-line)
    -   [Dessin d’une ligne avec GDI](#drawing-a-line-with-gdi)
    -   [Dessin d’une ligne avec GDI+ et l’interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Stylets, pinceaux, tracés, images et polices en tant que paramètres](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Surcharge de méthode](#method-overloading)
-   [Plus de position actuelle](#no-more-current-position)
-   [Méthodes distinctes pour dessiner et remplir](#separate-methods-for-draw-and-fill)
-   [Construction de régions](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contextes de périphérique, Handles et objets graphiques

Si vous avez écrit des programmes à l’aide de GDI (l’interface de périphérique graphique incluse dans les versions précédentes de Windows), vous êtes familiarisé avec l’idée d’un contexte de périphérique (DC). Un contexte de périphérique est une structure utilisée par Windows pour stocker des informations sur les fonctionnalités d’un périphérique d’affichage particulier et les attributs qui spécifient la façon dont les éléments sont dessinés sur cet appareil. Un contexte de périphérique pour un affichage vidéo est également associé à une fenêtre particulière sur l’écran. Tout d’abord, vous obtenez un handle vers un contexte de périphérique (HDC), puis vous transmettez ce handle comme argument aux fonctions GDI qui effectuent en fait le dessin. Vous transmettez également le handle comme argument aux fonctions GDI qui obtiennent ou définissent les attributs du contexte de périphérique.

Lorsque vous utilisez GDI+, vous n’avez pas à vous soucier des handles et des contextes de périphérique, comme vous le feriez avec GDI. Il vous suffit de créer un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , puis d’appeler ses méthodes dans le style orienté objet familier, MyGraphicsObject. DrawLine (*paramètres*). L’objet **Graphics** est au cœur de GDI+, tout comme le contexte de périphérique est au cœur de GDI. Le contexte de périphérique et l’objet **Graphics** jouent des rôles similaires, mais il existe des différences fondamentales entre le modèle de programmation basé sur les descripteurs et les contextes de périphérique (GDI) et le modèle orienté objet utilisé avec les objets **Graphics** (GDI+).

L’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , comme le contexte de périphérique, est associé à une fenêtre particulière à l’écran et contient des attributs (par exemple, le mode de lissage et l’indicateur de rendu de texte) qui spécifient la façon dont les éléments doivent être dessinés. Toutefois, l’objet **Graphics** n’est pas lié à un stylet, un pinceau, un tracé, une image ou une police comme contexte de périphérique. Par exemple, dans GDI, avant de pouvoir utiliser un contexte de périphérique pour dessiner une ligne, vous devez appeler [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) pour associer un objet Pen au contexte de périphérique. On parle alors de sélectionner le stylet dans le contexte de l’appareil. Toutes les lignes dessinées dans le contexte de périphérique utilisent ce stylet jusqu’à ce que vous sélectionnez un autre stylet. Avec GDI+, vous transmettez un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) en tant qu’argument à la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la classe **Graphics** . Vous pouvez utiliser un objet **Pen** différent dans chacune d’une série d’appels DrawLine sans avoir à associer un objet **Pen** donné à un objet **Graphics** .

## <a name="two-ways-to-draw-a-line"></a>Deux façons de dessiner une ligne

Les deux exemples suivants dessinent chacun une ligne rouge de largeur 3 à partir de l’emplacement (20, 10) à l’emplacement (200 100). Le premier exemple appelle GDI et le second appelle GDI+ via l’interface de classe C++.

-   [Dessin d’une ligne avec GDI](#drawing-a-line-with-gdi)
-   [Dessin d’une ligne avec GDI+ et l’interface de classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Dessin d’une ligne avec GDI

Pour dessiner une ligne avec GDI, vous avez besoin de deux objets : un contexte de périphérique et un stylet. Vous pouvez obtenir un handle vers un contexte de périphérique en appelant [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)et un handle à un stylet en appelant [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Ensuite, vous appelez [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) pour sélectionner le stylet dans le contexte de l’appareil. Vous définissez la position du stylet sur (20, 10) en appelant [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) , puis dessinez une ligne à partir de cette position de stylet sur (200, 100) en appelant **LineTo**. Notez que MoveToEx et [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) reçoivent tous deux **HDC** comme argument.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Dessin d’une ligne avec GDI+ et l’interface de classe C++

Pour dessiner une ligne avec GDI+ et l’interface de classe C++, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Notez que vous ne demandez pas à Windows les descripteurs de ces objets. Au lieu de cela, vous utilisez des constructeurs pour créer une instance de la classe **Graphics** (un objet **Graphics** ) et une instance de la classe **Pen** (un objet **Pen** ). Le dessin d’une ligne implique l’appel de la méthode [**Graphics ::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la classe **Graphics** . Le premier paramètre de la méthode **Graphics ::D rawline** est un pointeur vers votre objet **Pen** . Il s’agit d’un schéma plus simple et plus souple que la sélection d’un stylet dans un contexte de périphérique, comme indiqué dans l’exemple GDI précédent.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Stylets, pinceaux, tracés, images et polices en tant que paramètres

Les exemples précédents montrent que les objets [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) peuvent être créés et gérés séparément de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , qui fournit les méthodes de dessin. Les objets [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush), [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath), [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)et [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) peuvent également être créés et gérés séparément de l’objet **Graphics** . La plupart des méthodes de dessin fournies par la classe **Graphics** reçoivent un objet **Brush**, **GraphicsPath**, **image** ou **font** comme argument. Par exemple, l’adresse d’un objet **Brush** est passée comme argument à la méthode [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) , et l’adresse d’un objet **GraphicsPath** est passée comme argument à la méthode [**Graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . De même, les adresses des objets **image** et **font** sont passées aux méthodes [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) et [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) . Contrairement à GDI, vous pouvez sélectionner un pinceau, un tracé, une image ou une police dans le contexte de périphérique, puis passer un handle au contexte de périphérique en tant qu’argument d’une fonction de dessin.

## <a name="method-overloading"></a>Surcharge de méthode

La plupart des méthodes GDI+ sont surchargées ; autrement dit, plusieurs méthodes partagent le même nom, mais ont des listes de paramètres différentes. Par exemple, la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est présente sous la forme suivante :


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Les quatre variations [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) ci-dessus reçoivent un pointeur vers un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , les coordonnées du point de départ et les coordonnées du point de fin. Les deux premières variations reçoivent les coordonnées sous forme de nombres à virgule flottante, et les deux dernières variations reçoivent les coordonnées sous forme d’entiers. Les première et troisième variations reçoivent les coordonnées sous la forme d’une liste de quatre nombres distincts, tandis que les deuxième et quatrième versions reçoivent les coordonnées sous la forme d’un couple d’objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).

## <a name="no-more-current-position"></a>Plus de position actuelle

Notez que dans les méthodes [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) indiquées précédemment, le point de départ et le point de fin de la ligne sont reçus comme arguments. Il s’agit d’un écart par rapport au schéma GDI dans lequel vous appelez **MoveToEx** pour définir la position actuelle du stylet suivie de **LineTo** pour dessiner une ligne commençant à (**x1**, **Y1**) et se terminant à (**x2**, **Y2**). L’ensemble de GDI+ a abandonné la notion de position actuelle.

## <a name="separate-methods-for-draw-and-fill"></a>Méthodes distinctes pour dessiner et remplir

GDI+ est plus flexible que GDI lorsqu’il s’agit de dessiner les plans et de remplir l’intérieur des formes comme les rectangles. GDI a une fonction [rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) qui dessine le contour et remplit l’intérieur d’un rectangle tout en une seule étape. Le contour est dessiné avec le stylet actuellement sélectionné, et l’intérieur est rempli avec le pinceau actuellement sélectionné.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ a des méthodes distinctes pour dessiner le contour et remplir l’intérieur d’un rectangle. La méthode [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) de la [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a l’adresse d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) comme l’un de ses paramètres, et la méthode [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) a l’adresse d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) comme l’un de ses paramètres.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Notez que les méthodes [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) et [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) de GDI+ reçoivent des arguments qui spécifient le bord gauche, la largeur et la hauteur du rectangle. Cela diffère de la fonction[rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) GDI, qui accepte les arguments qui spécifient le bord gauche du rectangle, le bord droit, le haut et le bas. Notez également que le constructeur de la classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) dans GDI+ a quatre paramètres. Les trois derniers paramètres sont les valeurs de rouge, de vert et de bleu habituelles. le premier paramètre est la valeur alpha, qui spécifie dans quelle mesure la couleur dessinée est mélangée à la couleur d’arrière-plan.

## <a name="constructing-regions"></a>Construction de régions

GDI fournit plusieurs fonctions pour la création de régions : CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn et CreatePolyPolygonRgn. Vous vous attendez peut-être à ce que la classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) de GDI+ ait des constructeurs analogues qui acceptent des rectangles, des ellipses, des rectangles arrondis et des polygones comme arguments, mais ce n’est pas le cas. La classe **Region** dans GDI+ fournit un constructeur qui reçoit une référence d’objet [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) et un autre constructeur qui reçoit l’adresse d’un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . Si vous souhaitez construire une région basée sur une ellipse, un rectangle arrondi ou un polygone, vous pouvez facilement le faire en créant un objet **GraphicsPath** (qui contient une ellipse, par exemple), puis en passant l’adresse de cet objet **GraphicsPath** à un constructeur **Region** .

Avec GDI+, il est facile de former des zones complexes en combinant des formes et des tracés. La classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) a des méthodes [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) et [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) que vous pouvez utiliser pour augmenter une région existante avec un chemin d’accès ou une autre région. Une fonctionnalité intéressante du schéma GDI+ est qu’un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) n’est pas détruit lorsqu’il est passé comme argument à un constructeur **Region** . Dans GDI, vous pouvez convertir un chemin d’accès à une région avec la fonction [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) , mais le chemin d’accès est détruit dans le processus. En outre, un objet **GraphicsPath** n’est pas détruit quand son adresse est passée comme argument à une méthode Union ou INTERSECT. vous pouvez donc utiliser un chemin d’accès donné comme bloc de construction pour plusieurs régions distinctes. Cela est illustré par l'exemple suivant. Supposons que **onePath** est un pointeur vers un objet **GraphicsPath** (simple ou complexe) qui a déjà été initialisé.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
