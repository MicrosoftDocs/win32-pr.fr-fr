---
title: Portage des surfaces NURBS
description: Le tableau suivant répertorie les fonctions IRIS GL permettant de dessiner des surfaces NURBS et leurs fonctions OpenGL équivalentes.
ms.assetid: d34ac6af-55d7-4128-bcd9-3c910607895f
keywords:
- Portage de l’IRIS dans le GL, surfaces NURBS
- Portage à partir de IRIS GL, surfaces NURBS
- portage vers OpenGL à partir d’IRIS GL, surfaces NURBS
- Portage OpenGL depuis IRIS GL, surfaces NURBS
- Surfaces NURBS
- NURBS (non-uniform rational B-spline)
- B-spline rationnelle non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7260750db4d221743d3e764d6dd30e2de499383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127014005"
---
# <a name="porting-nurbs-surfaces"></a>Portage des surfaces NURBS

Le tableau suivant répertorie les fonctions IRIS GL permettant de dessiner des surfaces NURBS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                            | Signification                       |
|------------------|--------------------------------------------|-------------------------------|
| **bgnsurface**   | [**gluBeginSurface**](glubeginsurface.md) | Commence une définition de surface.  |
| **nurbssurface** | [**gluNurbsSurface**](glunurbssurface.md) | Spécifie les attributs de surface. |
| **endsurface**   | [**gluEndSurface**](gluendsurface.md)     | Termine une définition de surface.    |



 

Le tableau suivant répertorie les paramètres de l’IRIS dans le GL pour les types de surface et leurs paramètres OpenGL équivalents.



| Type de GL IRIS | Type OpenGL                 | Signification                                                |
|--------------|-----------------------------|--------------------------------------------------------|
| N \_ v3d       | Map2 du GL- \_ \_ vertex \_ 3         | Courbe polynomiale.                                      |
| N \_ V3DR      | Map2 du GL- \_ \_ vertex \_ 4         | Courbe rationnelle.                                        |
| N \_ C4D       | Map2 GL- \_ \_ couleur \_ 4          | Les points de contrôle définissent la surface de couleur dans le formulaire (R, G, B, A). |
| N \_ C4DR      |                             |                                                        |
| N \_ T2D       | \_Map2 de \_ texture \_ GL \_ 2 | Les points de contrôle sont des coordonnées de texture.                |
| N \_ T2DR      | \_Repère de \_ texture map2 GL \_ \_ 3 | Les points de contrôle sont des coordonnées de texture.                |
|              | Map2 GL- \_ \_ normal            | Les points de contrôle sont normaux.                            |



 

Pour plus d’informations sur les types d’évaluateurs disponibles, consultez [**glMap2**](glmap2.md).

L’exemple de code suivant dessine une surface NURBS rognée :


```C++
/* 
 *  trim.c 
 *  This program draws a NURBS surface in the shape of a 
 *  symmetrical hill, using both a NURBS curve and pwl 
 *  (piecewise linear) curve to trim part of the surface 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
GLfloat ctlpoints[4][4][3]; 
 
GLUnurbsObj *theNurb; 
 
/* 
 *  Initializes the control points of the surface to  
 *  a small hill. The control points range from -3 to  
 *  +3 in x, y, and z 
 */ 
void init_surface(void) 
{ 
    int u, v; 
    for (u = 0; u < 4; u++) { 
        for (v = 0; v < 4; v++) { 
            ctlpoints[u][v][0] = 2.0*((GLfloat)u - 1.5); 
            ctlpoints[u][v][1] = 2.0*((GLfloat)v - 1.5); 
 
            if ( (u == 1 || u == 2) && (v == 1 || v == 2)) 
                ctlpoints[u][v][2] = 3.0; 
            else 
                ctlpoints[u][v][2] = -3.0; 
        } 
    } 
} 
 
/*  Initialize material property and depth buffer 
 */ 
void myinit(void) 
{ 
    GLfloat mat_diffuse[] = { 0.6, 0.6, 0.6, 1.0 }; 
    GLfloat mat_specular[] = { 0.9, 0.9, 0.9, 1.0 }; 
    GLfloat mat_shininess[] = { 128.0 }; 
 
    glClearColor (0.0, 0.0, 0.0, 1.0); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_diffuse); 
    glMaterialfv(GL_FRONT, GL_SPECULAR, mat_specular); 
    glMaterialfv(GL_FRONT, GL_SHININESS, mat_shininess); 
 
    glEnable(GL_LIGHTING); 
    glEnable(GL_LIGHT0); 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glEnable(GL_AUTO_NORMAL); 
    glEnable(GL_NORMALIZE); 
 
    init_surface(); 
 
    theNurb = gluNewNurbsRenderer(); 
    gluNurbsProperty(theNurb, GLU_SAMPLING_TOLERANCE, 50.0); 
    gluNurbsProperty(theNurb, GLU_DISPLAY_MODE, GLU_FILL); 
} 
 
void display(void) 
{ 
    GLfloat knots[8] = {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat edgePt[5][2] = /* counter clockwise */ 
    {{0.0, 0.0}, {1.0, 0.0}, {1.0, 1.0}, {0.0, 1.0}, 
     {0.0, 0.0}}; 
    GLfloat curvePt[4][2] = /* clockwise */ 
    {{0.25, 0.5}, {0.25, 0.75}, {0.75, 0.75}, {0.75, 0.5}}; 
    GLfloat curveKnots[8] = 
        {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat pwlPt[4][2] = /* clockwise */ 
        {{0.75, 0.5}, {0.5, 0.25}, {0.25, 0.5}}; 
 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glPushMatrix(); 
    glRotatef(330.0, 1.,0.,0.); 
    glScalef (0.5, 0.5, 0.5); 
 
    gluBeginSurface(theNurb); 
    gluNurbsSurface(theNurb, 
            8, knots, 
            8, knots, 
            4 * 3, 
            3, 
            &ctlpoints[0][0][0], 
            4, 4, 
            GL_MAP2_VERTEX_3); 
    gluBeginTrim (theNurb); 
        gluPwlCurve (theNurb, 5, &edgePt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluBeginTrim (theNurb); 
        gluNurbsCurve (theNurb, 8, curveKnots, 2, 
                &curvePt[0][0], 4, GLU_MAP1_TRIM_2); 
        gluPwlCurve (theNurb, 3, &pwlPt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluEndSurface(theNurb); 
 
    glPopMatrix(); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLdouble)w/(GLdouble)h, 3.0, 8.0); 
 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity(); 
    glTranslatef (0.0, 0.0, -5.0); 
} 
 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 500, 500); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 




