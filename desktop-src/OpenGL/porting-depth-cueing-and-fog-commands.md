---
title: Cueing de profondeur de Portage et commandes de brouillard
description: Cueing de profondeur de Portage et commandes de brouillard
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Portage du GL IRIS, profondeur cueing
- Portage à partir de IRIS GL, profondeur cueing
- portage vers OpenGL à partir de IRIS GL, Depth cueing
- Portage OpenGL à partir de IRIS GL, profondeur cueing
- Portage de l’IRIS dans le GL, brouillard
- Portage à partir de IRIS GL, brouillard
- portage vers OpenGL à partir de IRIS GL, brouillard
- Portage OpenGL depuis IRIS GL, brouillard
- profondeur cueing
- brouillard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119138"
---
# <a name="porting-depth-cueing-and-fog-commands"></a>Cueing de profondeur de Portage et commandes de brouillard

Lorsque vous portez des cueing de profondeur et des commandes de brouillard, gardez les points suivants à l’esprit :

-   L’appel IRIS GL, **fogvertex**, définit un mode et les paramètres qui affectent ce mode. Dans OpenGL, vous appelez [**glFog**](glfog.md) une fois pour définir le mode, puis de nouveau deux fois ou plus pour définir différents paramètres.
-   Dans OpenGL, cueing de profondeur n’est pas une fonctionnalité distincte. Utilisez le brouillard linéaire à la place de Depth cueing. (Cette section fournit un exemple de la procédure à suivre). Les fonctions de la comptabilité IRIS suivantes n’ont pas d’équivalent OpenGL direct :

    **depthcue**

    **lRGBrange**

    **lshaderange**

    **getdcm**

-   Pour ajuster la qualité du brouillard, utilisez [**glHint**](glhint.md)( \_ indicateur de brouillard GL \_ ).

Le tableau suivant répertorie les fonctions IRIS GL pour la gestion du brouillard et de leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL         | Fonction OpenGL                                     | Signification                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| **fogvertex**            | [**glFog**](glfog.md)                              | Définit différents paramètres de brouillard.      |
| **fogvertex**(FG \_ )  | [**glEnable**](glenable.md) ( \_ voile GL)            | Active le brouillard.                     |
| **fogvertex**(FG \_ désactivé) | [**glDisable**](gldisable.md) ( \_ voile GL)          | Désactive le brouillard.                    |
| **depthcue**             | [**glFog**](glfog.md) (GL \_ brouillard \_ mod, GL \_ Linear) | Utilise le brouillard linéaire pour la profondeur cueing. |



 

Le tableau suivant répertorie les paramètres que vous pouvez passer à **glFog**.



| Paramètre de brouillard    | Signification                       | Default                  |
|------------------|-------------------------------|--------------------------|
| \_densité de brouillard GL \_ | Densité de brouillard.                  | 1.0                      |
| \_début du brouillard GL \_   | Distance proche du brouillard linéaire. | 0.0                      |
| \_fin du brouillard comptable \_     | Distance éloignée du brouillard linéaire.  | 1.0                      |
| \_index de brouillard GL \_   | Index de couleur de brouillard.              | 0.0                      |
| \_couleur de brouillard GL \_   | Couleur de brouillard RVBA.               | (0, 0, 0, 0)             |
| \_mode de brouillard GL \_    | Mode de brouillard.                     | Consultez le tableau suivant. |



 

Le paramètre de densité de brouillard de OpenGL diffère de celui de l’IRIS GL. Ils sont liés comme suit :

-   Si *fogMode* = EXP2
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))
-   Si *fogMode* = exp
     

    *openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))

où **sqrt** est l’opération racine carrée, **log** est le logarithme népérien, *irisGLfogDensity* est la densité de brouillard du GL d’IRIS et *openGLfogDensity* est la densité de brouillard OpenGL.

Pour basculer entre le calcul du brouillard en mode par pixel et le mode par vertex, utilisez [**glHint**](glhint.md)( \_ indicateur de brouillard GL \_ , *hintMode*). Deux modes d’indication sont disponibles :

-   \_Calcul de brouillard par pixel le plus agréable
-   \_Calcul du brouillard par vertex le plus rapide

Le tableau suivant répertorie les modes de brouillard d’IRIS GL et leurs équivalents OpenGL.



| Mode de brouillard du GL IRIS                       | Mode de brouillard OpenGL | Mode Hint                         | Signification                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| FG \_ VTX \_ exp, FG \_ pix \_ exp<br/>   | GL \_ exp         | GL \_ plus rapide, grand livre \_<br/> | Mode de brouillard lourd (par défaut).                |
| FG \_ VTX \_ EXP2, FG \_ pix \_ EXP2<br/> | \_EXP2 GL        | GL \_ plus rapide, grand livre \_<br/> | Mode voilé.                               |
| FG \_ VTX \_ lin, FG \_ pix \_ lin<br/>   | linéaire du GL \_      | GL \_ plus rapide, grand livre \_<br/> | Mode de brouillard linéaire. (À utiliser pour la profondeur cueing.) |



 

L’exemple de code suivant illustre la profondeur cueing dans OpenGL :


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





