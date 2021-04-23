---
title: Portage de polygones et de quadrilatères
description: Gardez les points suivants à l’esprit lors du Portage de polygones et de quadrilatères
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portage de l’IRIS dans le GL, quadrilatères
- Portage à partir de IRIS GL, quadrangulaires
- portage vers OpenGL à partir de IRIS GL, quadrangulaires
- Portage OpenGL à partir de IRIS GL, quadrangulaires
- fonctions de dessin, quadrilatères
- quadrilatères
- Portage de l’IRIS dans le GL, polygones
- Portage à partir de IRIS GL, polygones
- portage vers OpenGL à partir de IRIS GL, polygones
- Portage OpenGL à partir de IRIS GL, polygones
- fonctions de dessin, polygones
- polygones, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908457"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Portage de polygones et de quadrilatères

Gardez les points suivants à l’esprit lors du Portage de polygones et de quadrilatères :

-   Il n’existe aucun équivalent direct pour **concave**(**true**). Au lieu de cela, vous pouvez utiliser les routines de pavage dans le GLU, décrites dans [polygones le pavage](tessellating-polygons.md).
-   Les modes de polygone sont définis différemment.
-   Ces fonctions de dessin Polygon n’ont pas d’équivalent direct dans OpenGL : **la famille de** routines ; famille de routines **POLF** ; **PMV**, **PDR** et **PCLOS**; **rpmv** et **rpdr**; **SPLF**; et comfermeture.

Si votre code IRIS GL utilise ces fonctions, vous devrez réécrire le code à l’aide de [**glBegin**](glbegin.md)( \_ polygone GL).

Le tableau suivant répertorie les fonctions de dessin de polygones du GL IRIS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL         | Fonction OpenGL                                                    | Signification                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( \_ polygone GL)[**glEnd**](glend.md)   | Les vertex définissent la limite d’un polygone convexe simple.    |
|                          | **glBegin**(GL \_ quads)**glEnd**<br/>                       | Interprète les quadruples des sommets comme des quadrilatères.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)**glEnd**<br/> | Interprète les vertex comme des bandes liées de quadrilatères. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **en mode**             | [**glPolygonMode**](glpolygonmode.md)                             | Définit le mode dessin de polygone.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Dessine un rectangle.                                      |
| **sboxsboxf**<br/> |                                                                    | Dessine un rectangle aligné à l’écran.                       |



 

??

## <a name="porting-polygon-modes"></a>Portage des modes polygone

La fonction OpenGL [**glPolygonMode**](glpolygonmode.md) vous permet de spécifier le côté d’un polygone (l’arrière ou l’avant) auquel le mode s’applique. Sa syntaxe est la suivante :

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

où visage est l’un des éléments suivants :



|Valeur GLenum                      |  Signification                                                          |
|----------------------|------------------------------------------------------------|
| GL \_ frontal            | mode qui s’applique aux polygones frontaux                |
| Back. du GL \_             | mode qui s’applique aux polygones de l’arrière-plan                 |
| \_recto \_ et \_ Back GL | mode qui s’applique aux polygones avant et arrière |



 

Le \_ mode recto \_ et \_ verso GL est équivalent à la fonction Iris GL **polymode** . Le tableau suivant répertorie les modes de polygone du GL d’IRIS et leurs modes OpenGL équivalents.



| Mode de l’IRIS du GL | Mode OpenGL | Signification                                       |
|--------------|-------------|-----------------------------------------------|
| \_point Pym   | \_point GL   | Dessine des vertex en tant que points.                     |
| \_ligne Pym    | \_ligne GL    | Dessine des arêtes limites sous forme de segments de ligne.        |
| PYM \_ remplissage    | remplissage du GL \_    | Dessine l’intérieur du polygone rempli.                |
| PYM \_ creux  |             | Remplit uniquement les pixels intérieurs aux limites. |



 

## <a name="porting-polygon-stipples"></a>Portage du polygone stipples

Lorsque vous portagez IRIS GL Polygon stipples, gardez les points suivants à l’esprit :

-   OpenGL n’utilise pas de tables pour Polygon stipples ; un seul modèle stipple est conservé. Vous pouvez utiliser des listes d’affichage pour stocker différents modèles stipple.
-   La taille de l’image bitmap OpenGL Polygon stipple est toujours un modèle 32 x 32.
-   L’encodage stipple est affecté par [**glPixelStore**](glpixelstore-functions.md).

Pour plus d’informations sur le portage des stipples Polygon, consultez [Portage d’opérations de pixels](porting-pixel-operations.md).

Le tableau suivant répertorie les fonctions stipple et les fonctions OpenGL équivalentes de l’IRIS GL.



| Fonction IRIS GL | Fonction OpenGL                                    | Signification                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Définit le modèle stipple.                             |
| **setpattern**   |                                                    | OpenGL conserve un seul modèle Polygon stipple.        |
| **GetPattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Retourne la bitmap stipple (utilisée pour retourner un index). |



 

Dans OpenGL, vous activez et désactivez Polygon stippling en transmettant GL \_ Polygon \_ STIPPLE en tant que paramètre pour [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).

L’exemple de code OpenGL suivant illustre stippling Polygon :


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>Portage de polygones fractionnés

Dans IRIS GL, vous utilisez **concave**(**true**), puis **bgnpolygon** pour dessiner des polygones concave. Le GLU OpenGL comprend des fonctions que vous pouvez utiliser pour dessiner des polygones concave.

**Pour dessiner un polygone concave avec OpenGL**

1.  Créez un objet de pavage.
2.  Définissez les rappels qui seront utilisés pour traiter les triangles générés par le du paveur.
3.  Spécifiez le polygone concave à fractionnér.

Le tableau suivant répertorie les fonctions OpenGL permettant de dessiner des polygones fractionnés.



| Fonction OpenGL GLU                        | Signification                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Crée un objet de pavage.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Supprime un objet de pavage.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Commence la spécification du polygone.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Spécifie un sommet de polygone dans un contour.                           |
| [**gluNextContour**](glunextcontour.md)   | Indique que la série de vertex suivante décrit un nouveau contour. |
| [**gluEndPolygon**](gluendpolygon.md)     | Met fin à la spécification Polygon.                                    |



 

 

 





