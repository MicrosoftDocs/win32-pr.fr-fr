---
description: Un ventilateur triangulaire est semblable à une bande triangulaire, sauf que tous les triangles partagent un sommet, comme indiqué dans l’illustration suivante.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventilateurs triangulaires (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570465"
---
# <a name="triangle-fans-direct3d-9"></a>Ventilateurs triangulaires (Direct3D 9)

Un ventilateur triangulaire est semblable à une bande triangulaire, sauf que tous les triangles partagent un sommet, comme indiqué dans l’illustration suivante.

![illustration d’un ventilateur triangulaire](images/trifan.gif)

Le système utilise les vertex v2, v3 et V1 pour dessiner le premier triangle. v3, V4 et V1 pour dessiner le deuxième triangle ; v4, V5 et V1 pour dessiner le troisième triangle ; et ainsi de suite. Lorsque l’ombrage plat est activé, le système ombre le triangle avec la couleur de son premier vertex.

L’illustration suivante représente un ventilateur à triangle rendu.

![illustration d’un ventilateur à triangle rendu](images/tfan2.gif)

Le code suivant montre comment créer des vertex pour ce ventilateur de triangle.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



L’exemple de code ci-dessous montre comment restituer ce ventilateur à triangle dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Les ventilateurs de triangle ne sont pas pris en charge dans Direct3D 10 ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
