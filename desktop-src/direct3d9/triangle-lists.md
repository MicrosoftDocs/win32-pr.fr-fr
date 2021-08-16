---
description: Une liste triangulaire est une liste de triangles isolés. Ils peuvent être ou ne pas se rapprocher les uns des autres. Une liste de triangles doit avoir au moins trois vertex et le nombre total de vertex doit être divisible par trois.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listes de triangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0f9df4d9a0a6d883abd2ccf6b4f3e86c03bb54bcc404901b3c3fa6d10ede03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797435"
---
# <a name="triangle-lists"></a>Listes de triangles

Une liste triangulaire est une liste de triangles isolés. Ils peuvent être ou ne pas se rapprocher les uns des autres. Une liste de triangles doit avoir au moins trois vertex et le nombre total de vertex doit être divisible par trois.

Utilisez des listes de triangles pour créer un objet composé de pièces disjointes. Par exemple, une façon de créer un mur de champ de force dans un jeu 3D consiste à spécifier une grande liste de petits triangles non connectés. Appliquez ensuite un matériau et une texture qui semblent émettre de la lumière dans la liste de triangles. Chaque triangle du mur semble briller. La scène derrière le mur devient partiellement visible à travers les intervalles entre les triangles, car un joueur peut s’attendre à voir un champ force.

Les listes de triangles sont également utiles pour créer des primitives qui ont des bords tranchants et qui sont ombrées avec l’ombrage Gouraud. Consultez [vecteurs normaux de face et vertex (Direct3D 9)](face-and-vertex-normal-vectors.md).

L’illustration suivante représente une liste de triangles rendue.

![illustration d’une liste de triangles rendue](images/trilist.png)

Le code suivant montre comment créer des vertex pour cette liste de triangles.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



L’exemple de code ci-dessous montre comment afficher cette liste de triangles dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



Vous pouvez également utiliser des bandes triangulaires pour afficher des triangles qui ne sont pas connectés les uns aux autres. Pour ce faire, spécifiez un triangle dégenerate (autrement dit, un triangle avec une taille nulle) dans la liste ; Cette opération crée une ligne entre les deux triangles qui n’apparaît pas pendant le rendu. Par exemple, pour afficher uniquement le premier et le dernier triangle de l’exemple précédent, initialisez la mémoire tampon de vertex avec les vertex suivants :


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
