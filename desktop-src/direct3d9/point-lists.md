---
description: Une liste de points est une collection de vertex qui sont rendus sous forme de points isolés. Votre application peut les utiliser dans des scènes 3D pour des champs en étoile, ou des lignes en pointillés sur la surface d’un polygone.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listes de points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746780"
---
# <a name="point-lists"></a>Listes de points

Une liste de points est une collection de vertex qui sont rendus sous forme de points isolés. Votre application peut les utiliser dans des scènes 3D pour des champs en étoile, ou des lignes en pointillés sur la surface d’un polygone.

L’illustration suivante représente une liste de points rendue.

![illustration d’une liste de points](images/pointlst.png)

Votre application peut appliquer des matériaux et des textures à une liste de points. Les couleurs de la texture ou du matériau apparaissent uniquement aux points dessinés, et pas entre les points.

Le code suivant montre comment créer des vertex pour cette liste de points.


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



L’exemple de code ci-dessous montre comment afficher cette liste de points dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
