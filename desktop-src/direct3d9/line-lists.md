---
description: Une liste de lignes est une liste de segments de ligne droite isolés.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Listes de lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606793"
---
# <a name="line-lists"></a>Listes de lignes

Une liste de lignes est une liste de segments de ligne droite isolés. Les listes de lignes sont utiles pour des tâches telles que l’ajout de Sleet ou de la pluie lourde à une scène 3D. Les applications créent une liste de lignes en remplissant un tableau de vertex. Notez que le nombre de vertex dans une liste de lignes doit être un nombre pair supérieur ou égal à deux.

L’illustration suivante montre une liste de lignes restituées.

![illustration d’une liste de lignes](images/linelst.png)

Vous pouvez appliquer des matériaux et des textures à une liste de lignes. Les couleurs de la texture ou du matériau s’affichent uniquement le long des lignes dessinées, et non à un point situé entre les lignes.

Le code suivant montre comment créer des vertex pour cette liste de lignes.


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



L’exemple de code ci-dessous montre comment afficher une liste de lignes dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
